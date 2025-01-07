<b>NOTANONcurrentPending</b> is a file containing a short (1-few page) report for each team member, describing their current and pending (still under review) research grants, a section typically required by most grant solicitations. If the box is checked under "funding status?" column for a person on the PERSONNEL & FTE page, then that person's current/pending form will be generated and included as part of this file. All current/pending reports are formatted to have a consistant appearance. 

The information for the report is taken from that person's individual WorPT biosketch google sheet. The last page in that google sheet
is where the list of grants, and their statuses, are written.  The WorPT script will copy every grant that is still either active or has a status
indicating that no information regarding selection has yet been obtained, and will format those grants into this current/pending form. The NOTANONcurrentPending WorPT file can serve as the "Current & Pending Funding" section of your proposal.  

NOTE: WorPT biosketch spreadsheet files should be kept up-to-date so that the information that is extracted for both the current/pending and bio-sketch sections of a proposal have valid and current information.

<font size="3">WorPT table example: <b>NOTANONcurrentPending</b></font>
<br>
<img src="https://lh3.googleusercontent.com/d/1hQWaFzw0-oolj-ZgvmulSnWuO5ptYoTM" width=30%>
<hr>
<b>HOW TO USE:</b>
<ol>
<li><b>Special WorPT Packages</b> [<i>one-time-only task</i>] Copy/paste the special packages in preamble of your document, if you haven't done so previously. (see https://github.com/pmarcum/WorPT-Work-Plan-Tool-4-proposals/blob/main/WorPTpackages for more info).</li>
<li><mark><b>How To Put File Contents Into Your Document</b></mark> [<i>do once for inclusion of this file</i>] 
<ol>
<li>COPY the lines in the code block below, then</li>
<li>PASTE into your document WHERE you want the content to appear, then</li>
<li>MODIFY the editable lines you just pasted in your document as needed. The lines that may be edited (or even deleted altogether if not wanted) are indicated by highlight below. </li>
</ol>
   
<pre><code>
\newpage       % You can comment out or use \clearpage instead
\include{do_NOT_manually_edit/table_NOTANONcurrentPending}  % if you used a different folder name, replace do_NOT_Manually_edit with the correct name
<mark>% Put customizations for NOTANONcurrentPending HERE</mark>
\begin{NOTANONcurrentPending}
\end{NOTANONcurrentPending}  
</code></pre>
</li>

<li><b>Customize appearance</b> [<i>do as many times as needed</i>]
The default settings produce a nice-looking file, so you probably won't have to do any customization for this file. But if desired, you can change colors, font style and spacing using additional lines that are copy/pasted into your document. Specifically: 
<ol>
<li>COPY any or all lines in the code block below that are related to the formatting parameter that you want to edit. The lines below show default values. You will edit those values to make desired changes.</li>
<li>PASTE the copied lines into your document at the "% Put customizations for NOTANONcurrentPending HERE" line in the code that you copy/pasted in Step 2. Most importantly, the desired formatting lines should be pasted somewhere <b>between</b> the \include{do_NOT_manually_edit/table_NOTANONcurrentPending} and \begin{NOTANONcurrentPending} lines. </li>
<li>EDIT the pasted lines in your document, as desired. Some examples are given at the bottom of this page.</li>
NOTE: you can PICK AND CHOOSE the lines you want to paste into your document; you do not have to copy/paste all of the below lines!
</ol>
<b>The below lines will help you change column widths. Highlights indicate what can be edited:</b>    
<pre><code>
\dev\LeftSideWidth{<mark>1.5in</mark>}             % width of left side column
\dev\RightSideWidth{<mark>5.0in</mark>}            % width of right side column
</code></pre>

<b>The below lines will help you change color scheme, font style, if desired. Highlights indicate what can be edited:</b>    
<pre><code>
\def\NameBannerColor{<mark>Blue</mark>}            % Current/Pending top banner color
\def\NameBannerColor{<mark>White</mark>}           % Current/Pending top banner font color
\def\NameBannerBoldface#1{<mark>\textbf</mark>{#1}} % boldface banner text
</code></pre>
   
<b>The below change the appearance of section dividers (e.g., "Current Support", "Pending Grant Support"):</b>
<pre><code>
\def\SectionColor{<mark>lightgray</mark>}          % "Current Support" & "Pending Grant Support" section divider color
\def\SectionFontColor{<mark>Black</mark>}          % "Current Support" & "Pending Grant Support" section divider font color
\def\SectionBoldface#1{<mark>\textbf</mark>{#1}}   % "Current Support" & "Pending Grant Support" section divider font style
</code></pre>
   
<b>The below changes the font color of the "(this proposal)" note that appears by the proposal to be submitted</b>, where it is listed in the "PENDING" list, if that proposal is instructed to be included in the PENDING list. If the box is checked for "Include this proposal in funding status?" on the GENERAL INFO page in the WorPT spreadsheet, then the proposal of interest will be included in the PENDING list with this tag attached. 
<pre><code>
\def\ThisProposalColor{<mark>NavyBlue</mark>}      % "this proposal" font color in "pending" section
</code></pre>

<b>The below changes the font style of the left column, lists of grant descriptors like "TItle", "Source of Support", etc.</b>
<pre><code>
\def\LeftBoldface#1{<mark>\textbf</mark>{#1}}      % boldface left column text
</code></pre>

<b>The below table preamble gives you considerably MORE control over table layout than just changing parameter values.</b>
Copy/paste the below if you want to do things like remove or add vertical lines or change a column from left-alignment to center-aligned, for example. You can replace the \LeftSideWidth and other parameters with hard-coded numbers if desired, and change the "p" to other alignment modes. You can change anything that is in highlight. Things that should NOT be changed (otherwise, the LaTeX will break) are the "T" variable and number of columns. 
<pre><code>
\newcolumntype{T}{
  <mark>|p</mark>{<mark>\LeftSideWidth</mark>}     % grant descriptors, e.g. "Title", "Source of Support", etc.
  <mark>|p</mark>{<mark>\RightSideWidth</mark>}|   % right side, giving details for each descriptor
}
</code></pre> 

</li>

<li><b>Examples</b>
The below is an example of how one can change the appearance of the contents within a LaTeX document. After copy/pasting the code to incorporate the file contents into my document, I decided to change the color of the name banners from blue to black, the font color to yellow, and to italicize the font in the name banner.  I also needed to make the right column a bit wider. To accomplish these tasks, I copy/pasted the relevant formatting lines that control these items and then edited my preferences. Here is a peek at what my LaTeX document looks like:  
<pre><code>
\newpage       % You can comment out or use \clearpage instead
\include{do_NOT_manually_edit/table_NOTANONcurrentPending}

% Put customizations for NOTANONcurrentPending HERE
    
\def\NameBannerColor{Black}            % Current/Pending top banner color
\def\NameBannerColor{Yellow}           % Current/Pending top banner font color
\def\NameBannerBoldface#1{\emph{#1}}   % boldface banner text
\dev\RightSideWidth{5.3in}             % width of right side column

\begin{NOTANONcurrentPending}
\end{NOTANONcurrentPending}
</code></pre>
NOTE: To return to default values, all I have to do is comment-out (put a "%" at the line's beginning) the "\def" formatting lines that I pasted. 
</li>

<li><b>NUCLEAR OPTION:</b>
If you just cannot get the content to look like you want it to look, you can always copy/paste the entire table_NOTANONcurrentPending file that appears in the WorPT subfolder, into your document, and then edit at-will.  Some of the WorPT files involve complicated LaTeX code, so be sure that you have a good mastery of LaTeX and know what you are doing before implementing this option!
</li>
</ol>
