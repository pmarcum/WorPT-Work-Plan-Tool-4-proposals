<b>NOTANONcurrentPending</b> is a file containing a short (1-few page) report for each team member, describing their current and pending (still under review) research grants, a section typically required by most grant solicitations. If the box is checked under "funding status?" column for a person on the PERSONNEL & FTE page, then that person's current/pending form will be generated and included as part of this file. All current/pending reports are formatted to have a consistant appearance. 

The information for the report is taken from that person's individual WorPT biosketch google sheet. The last page in that google sheet
is where the list of grants, and their statuses, are written.  The WorPT script will copy every grant that is still either active or has a status
indicating that no information regarding selection has yet been obtained, and will format those grants into this current/pending form. The NOTANONcurrenPending WorPT file can serve as the "Current & Pending Funding" section of your proposal.  

NOTE: WorPT biosketch spreadsheet files should be kept up-to-date so that the information that is extracted for both the current/pending and bio-sketch sections of a proposal have valid and current information.

<font size="3">WorPT table example: <b>NOTANONcurrentPending</b></font>
<br>
<img src="https://lh3.googleusercontent.com/d/1hQWaFzw0-oolj-ZgvmulSnWuO5ptYoTM" width=40%>
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
\include{\WorPTfolder/table_NOTANONcurrentPending}
<mark>% Put customizations for NOTANONcurrentPending HERE</mark>
\begin{NOTANONcurrentPending}
\end{NOTANONcurrentPending}  
</code></pre>
</li>

<li><b>Customize appearance</b> [<i>do as many times as needed</i>]
The default settings produce a nice-looking file, so you probably won't have to do any customization for this file. But if desired, you can change colors, font style and spacing using additional lines that are copy/pasted into your document. Specifically: 
<ol>
<li>COPY any or all lines in the code block below that are related to the formatting parameter that you want to edit. The lines below show default values. You will edit those values to make desired changes.</li>
<li>PASTE the copied lines into your document at the "% Put customizations for NOTANONcurrentPending HERE" line in the code that you copy/pasted in Step 2. Most importantly, the desired formatting lines should be pasted somewhere <b>between</b> the \include{\WorPTfolder/table_NOTANONcurrentPending} and \begin{NOTANONcurrentPending} lines. </li>
<li>EDIT the pasted lines in your document, as desired. Some examples are given at the bottom of this page.</li>
NOTE: you can PICK AND CHOOSE the lines you want to paste into your document; you do not have to copy/paste all of the below lines!
</ol>
<b>The below lines are what you will most likely need to copy/paste, to get your column widths just right. Highlights indicate what can be edited:</b>    
<pre><code>
\def\NameColor{<mark>Blue</mark>}                          % font color of name/role appearing at top of biosketch
\def\NameSize{<mark>\large</mark>}                         % font size of name/role
\def\NameBoldface#1{<mark>\textbf</mark>{#1}}              % boldface name/role
\def\LabelBoldface#1{<mark>\textbf</mark>{#1}}             % boldface "Education",... labels
</code></pre>
<b>Use the following to compress or make more vertical space between the "Education", "Appointments", etc sections:</b>
<pre><code>
\def\SectionSpacing{\par \vspace{<mark>-0.5em</mark>}}     % vertical spacing bet/ categories
</code></pre>
<b>Use the below to change the symbol that marks the beginning of each entry in the publication list:</b>
<pre><code>
\def\PublicationBullet{<mark>\scriptsize{$\bullet$}{\hspace{-0.3em}}</mark>}
</code></pre>
</li>

<li><b>Examples</b>
The below is an example of how one can change the appearance of the contents within a LaTeX document. After copy/pasting the code to incorporate the file contents into my document, I decided to change the color of the names from the default blue color, to Black and also to italicize the names. I copy/pasted the 2 formatting lines that control these items and then edited my preferences. Here is a peek at what my LaTeX document looks like:  
<pre><code>
\include{\WorPTfolder/NOTANONcurrentPending}
    
\def\NameBoldface#1{\emph{#1}}              % boldface name/role
\def\NameColor{Black}                          % font color of name/role

\begin{NOTANONcurrentPending}
\end{NOTANONcurrentPending}
</code></pre>
NOTE: To return to default values, all I have to do is comment-out (put a "%" at the line's beginning) the "\def" formatting lines that I pasted. 
</li>

<li><b>NUCLEAR OPTION:</b>
If you just cannot get the content to look like you want it to look, you can always copy/paste the entire table_NOTANONcurrentPending file that appears in the WorPT subfolder, into your document, and then edit at-will.  Some of the WorPT files involve complicated LaTeX code, so be sure that you have a good mastery of LaTeX and know what you are doing before implementing this option!
</li>
</ol>
