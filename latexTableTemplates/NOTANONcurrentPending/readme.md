<!--------------------------------------
   SCREEN SHOT
--------------------------------------->
<table>
<tr>
<td>
<font size="3"><b>NOTANONcurrentPending</b></font>
<br>
<img src="https://lh3.googleusercontent.com/d/1hQWaFzw0-oolj-ZgvmulSnWuO5ptYoTM" width=70%>
</td>
<td>
<details>
<summary><b>NOTANONcurrentPending</b> (description)</summary>
<b>NOTANONcurrentPending</b> is a file containing a short (1-few page) report for each team member, describing their current and pending (still under review) research grants, a section typically required by most grant solicitations. If the box is checked under "funding status?" column for a person on the PERSONNEL & FTE page, then that person's current/pending form will be generated and included as part of this file. All current/pending reports are formatted to have a consistant appearance. <br>
The information for the report is taken from that person's individual WorPT biosketch google sheet. The last page in that google sheet
is where the list of grants, and their statuses, are written.  The WorPT script will copy every grant that is still either active or has a status
indicating that no information regarding selection has yet been obtained, and will format those grants into this current/pending form. The NOTANONcurrentPending WorPT file can serve as the "Current & Pending Funding" section of your proposal. <br>
NOTE: WorPT biosketch spreadsheet files should be kept up-to-date so that the information that is extracted for both the current/pending and bio-sketch sections of a proposal have valid and current information.
</details>
</td>
</tr>
</table>
<hr>

<!--------------------------------------
   HOW TO USE
--------------------------------------->
<b>HOW TO USE:</b>

<!-- - - - - - - - - - - - - - - - - - - - - - - - - - - - 
             Special Packages
- - - - - - - - - - - - - - - - - - - - - - - - - - - - -->
<details>
<summary><b>Special WorPT Packages</b> [<i>one-time-only task</i> for inclusion of any/all WorPT files]</summary>
Copy/paste the special packages in preamble of your document, if you haven't done so previously. (see https://github.com/pmarcum/WorPT-Work-Plan-Tool-4-proposals/blob/main/WorPTpackages for more info).
</details>

<!-- - - - - - - - - - - - - - - - - - - - - - - - - - - - 
             Putting File Contents Into Document
- - - - - - - - - - - - - - - - - - - - - - - - - - - - -->
<details>
<summary><mark><b>How To Put File Contents Into Your Document</b></mark> [<i>one-time-only task for inclusion of this file</i>]</summary> 
<ol>
<li>COPY the lines in the code block below, then</li>
<li>PASTE into your document WHERE you want the content to appear, then</li>
<li>MODIFY the editable lines you just pasted in your document as needed. The lines that may be edited (or even deleted altogether if not wanted) are indicated by highlight below. </li><br>
Refer to <b>Customizations</b> section below to add personal preferences in the gap between \expinput and \begin{NOTANONcurrentPending} lines below.
</ol>
   
<pre><code>
%:::::::::::::: start NOTANONcurrentPending ::::::::::::::::
\clearpage            % [optional] (could instead use \newpage, or comment out)
\expinput{<mark>do_NOT_manually_edit</mark>/NOTANONcurrentPending} % reset file parameters

\begin{NOTANONcurrentPending}
\end{NOTANONcurrentPending}  
%::::::::::::::: end NOTANONcurrentPending :::::::::::::::::
</code></pre>

</details>

<!-- - - - - - - - - - - - - - - - - - - - - - - - - - - - 
             Customizations
- - - - - - - - - - - - - - - - - - - - - - - - - - - - -->
<details>
<summary><b>Customize appearance</b> [<i>do as many times as needed</i>]</summary>
The default settings for this file produce a nice-looking bio-sketch section without any additional manual manipulation, so you probably won't have to do any customization for this file. But if desired, you can change colors, font style and spacing using additional lines that are copy/pasted into your document. Specifically: 
<ol>
<li>COPY any or all lines in the code block below that are related to the formatting parameter that you want to edit. The lines below show default values. You will edit those values to make desired changes.</li>
<li>PASTE the copied lines into your document into the gap <b>between</b> the \expinput and \begin{NOTANONcurrentPending} lines. </li>
<li>EDIT the pasted lines in your document, as desired.</li>
NOTE: The lines are grouped into categories to help you locate what you need. You can PICK AND CHOOSE the lines you want to paste into your document; you do not have to copy/paste all of the lines below (unless noted) and do not have to copy all lines within a group.<br>
<i>Highlights indicate what parts of the commands can be edited without breaking your LaTeX code.</i><br>
You can just comment out your added lines and recompile the document, if you want to return to default values.
</ol>

<!-- . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                              Options   
<!-- . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . -->
<table>
   
<tr>
<td><b>Column width adjustments</b></td>
<td><pre><code>
\def\LeftSideWidth{<mark>1.5in</mark>}  % left side column width
\def\RightSideWidth{<mark>5.0in</mark>} % right side column width
</code></pre>
<details>
<summary>reference image</summary>
<img src="https://lh3.googleusercontent.com/d/1SAA_MZ9p1gkPKWXVDJ-46qNdm2IXU1yB" width=30%>
</details>
</td>
</tr>
 
<tr>
<td><b>Font color and fontstyle</b></td>
<td><pre><code>
\def\NameBannerColor{<mark>Blue</mark>}              % Current/Pending top banner color
\def\NameBannerFontColor{<mark>White</mark>}             % Current/Pending top banner font color
\def\NameBannerFontstyle#1{<mark>\textbf</mark>{#1}} % boldface banner text
</code></pre>
<details>
<summary>reference image</summary>
<img src="https://lh3.googleusercontent.com/d/1FBgOkOroeONRwE3tkE6pqVinOJX0zX61" width=30%>
</details>
</td>
</tr>
   
<tr>
<td><b>Color and font style of section dividers</b></td>
<td><pre><code>
\def\SectionColor{<mark>lightgray</mark>}         % "Current Support","Pending Grant Support" section divider color
\def\SectionFontColor{<mark>Black</mark>}         % "Current Support","Pending Grant Support" section divider font color
\def\SectionFontstyle#1{<mark>\textbf</mark>{#1}} % "Current Support","Pending Grant Support" section divider font style
</code></pre>
<details>
<summary>reference image</summary>
<img src="https://lh3.googleusercontent.com/d/1Q6fAYXGcZgAlUA6MFaFjipEnR7sy2OS-" width=30%>
</details>
</td>
</tr>
   
<tr>
<td><b>Font color of "this proposal" tag</b></td>
<td>
If box is checked for "Include this proposal in funding status?" on the GENERAL INFO page in the WorPT spreadsheet, then this proposal will be included in PENDING list with this "this proposal" tag attached. 
<pre><code>
\def\ThisProposalColor{<mark>NavyBlue</mark>}  % "this proposal" font color in "pending" section
</code></pre>
<details>
<summary>reference image</summary>
<img src="https://lh3.googleusercontent.com/d/1ELG8UNriHu4q-GnxX0htOkY1oF_DHFHA" width=30%>
</details>
</td>
</tr>

<tr>
<td><b>Font style of grant descriptors in left colum</b></td>
<td><pre><code>
\def\LeftFontstyle#1{<mark>\textbf</mark>{#1}} % boldface left column text
</code></pre>
<details>
<summary>reference image</summary>
<img src="https://lh3.googleusercontent.com/d/1OSAyoNQ7v1ODSW6MOGNzcY906PgI4vL2" width=30%>
</details>
</td>
</tr>

<tr>
<td><b>Table preamble - full control!</b></td>
<td>
Use table preamble for more control over table layout (removing/adding vertical lines, changing column alignment, etc).<br>
Copy/paste the ENTIRE below code in order to change default table preamble.<br>
<u>IMPORTANT</u> Most of table preamble can be changed EXCEPT <i>do <b>NOT</b> change "T" variable, and preserve the number of columns</i>
(eg, make sure that any 'p' that is removed is replaced by another alignment code). You may retain the parameters below (like \LeftSideWidth) and
define them separately as the above customization options show, or replace them entirely with hard-coded numbers. 
<pre><code>
\newcolumntype{T}{
  <mark>|p{\LeftSideWidth}</mark>    % grant descriptors, e.g. "Title", "Source of Support", etc.
  <mark>|p{\RightSideWidth}|</mark>  % right side, giving details for each descriptor
}
</code></pre></td>
</tr>
</table>
</details>

<!--------------------------------------
   EXAMPLES 
--------------------------------------->
<details>
<summary><b>Examples</b></summary>
The below is an example of how one can change the appearance of the contents within a LaTeX document. After copy/pasting the code to incorporate the file contents into my document, I decided to change the color of the name banners from blue to black, the font color to yellow, and to italicize the font in the name banner.  I also needed to make the right column a bit wider. To accomplish these tasks, I copy/pasted the relevant formatting lines that control these items and then edited my preferences. Here is a peek at what my LaTeX document looks like:  

<!--     INSERT IMAGE -->

NOTE: To return to default values, all I have to do is comment-out (put a "%" at the line's beginning) the "\def" formatting lines that I pasted. 
</details>

<!--------------------------------------
   NUCLEAR OPTION 
--------------------------------------->
<details>
<summary><b>NUCLEAR OPTION</b> <i>[when nothing else works]</i></summary>
If you just cannot get the table to look like you want it to look, you can always copy/paste the entire NOTANONcurrentPending.tex file that appears in the WorPT subfolder, into your document, and then edit at-will.  Some of the WorPT files involve complicated LaTeX code, so be sure that you have a good mastery of LaTeX and know what you are doing before implementing this option!
</details>
