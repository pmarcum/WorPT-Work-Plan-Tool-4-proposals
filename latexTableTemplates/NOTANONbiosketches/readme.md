<!--------------------------------------
   SCREEN SHOT
--------------------------------------->
<table>
<tr>
<td>
<font size="3"><b>NOTANONbiosketches</b></font>
<br>
<img src="https://lh3.googleusercontent.com/d/1f3XxoAT5680nxNbcwWk4uifOvXdytuUh" width=60%>
</td>
<td>
<details>
<summary><b>NOTANONbiosketches</b> (description)</summary>
<b>NOTANONbiosketches</b> is NOT a table, but rather a tex file containing a short (1-page) CV for each team member who is indicated as needing to have a biosketch on the PERSONNEL & FTE page. If the box is checked under "bio sketch?" column for a person, then that person's bio sketch will be generated and included as part of this file. All biosketches are formatted to have a consistant appearance.  The information for this file is extracted from each person's individual WorPT biosketch google sheet. Checked boxes in that sheet indicate what publications and awards to mention, etc., customizing for this particular proposal. The NOTANONbiosketches WorPT file can serve as the "bio sketches" section of your proposal.<br>
NOTE: Biosketch files should be kept up-to-date so that the information that is extracted for both the current/pending and bio-sketch
sections of a proposal have valid and current information.
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
<summary><b>Special WorPT Packages</b> [<i>SKIP if you've already done this for previous WorPT file!</i>]</summary>
Copy/paste the special packages in preamble of your document, if you haven't done so previously. (see https://github.com/pmarcum/WorPT-Work-Plan-Tool-4-proposals/blob/main/latexTableTemplates/WorPTpackages/readme.md for more info).
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
Refer to <b>Customizations</b> section below to add personal preferences in the gap between \expinput and \begin{NOTANONbiosketches} lines below.
</ol>
   
<pre><code>
\newpage          % [optional] (could instead use \clearpage, or comment out)
\expinput{<mark>do_NOT_manually_edit</mark>/NOTANONbiosketches} % reset file parameters
<mark>

</mark>\begin{NOTANONbiosketches}
\end{NOTANONbiosketches}  
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
<li>PASTE the copied lines into your document at the "% Put customizations for NOTANONbiosketches HERE" line in the code that you copy/pasted in Step 2. Most importantly, the desired formatting lines should be pasted somewhere <b>between</b> the \include{do_NOT_manually_edit/NOTANONbiosketches} and \begin{NOTANONbiosketches} lines. </li>
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
<td><b>Font color and fontstyle</b></td>
<td><pre><code>
\def\NameColor{<mark>Blue</mark>} % font color of name/role at top of biosketch
\def\NameSize{<mark>\large</mark>}             % font size of name/role
\def\NameFontstyle#1{<mark>\textbf</mark>{#1}}  % boldface name/role
\def\LabelFontstyle#1{<mark>\textbf</mark>{#1}} % boldface "Education",... labels
</code></pre>
<details>
<summary>reference image</summary>
<img src="https://lh3.googleusercontent.com/d/1vt_FwYDfmmGgSDPFmmYpQbH4EDXOExaN" width=30%>
</details>
</td>
</tr>
   
<tr>
<td><b>Table compactness</b></td>
<td><pre><code>
\def\SectionSpacing{\par \vspace{<mark>-0.5em</mark>}} % vertical spacing bet/ categories
</code></pre>
<details>
<summary>reference image</summary>
<img src="https://lh3.googleusercontent.com/d/1TxGBbXY86Dwx5aXcPwpQC0dHzUr6diaV" width=30%>
</td>
</details>
</tr>

<tr>
<td><b>Symbol choice for publication list</b></td>
<td><pre><code>
\def\PubSym{<mark>\scriptsize{$\bullet$}{\hspace{-0.3em}}</mark>} % symbol in front of pubs
</code></pre>
<details>
<summary>reference image</summary>
<img src="https://lh3.googleusercontent.com/d/1ej8_jQPTlaiychgpRTfm32jH-gesh0Vl" width=30%>
</details>
</td>
</tr>
</table>
</details>

<!--------------------------------------
   EXAMPLES 
--------------------------------------->
<details>
<summary><b>Examples</b></summary>
The below is an example of how one can change the appearance of the contents within a LaTeX document. After copy/pasting the code to incorporate the file contents into my document, I decided to change the color of the names from the default blue color, to Black and also to italicize the names. I copy/pasted the 2 formatting lines that control these items and then edited my preferences. Here is a peek at what my LaTeX document looks like:  

<!--     INSERT IMAGE -->

NOTE: To return to default values, all I have to do is comment-out (put a "%" at the line's beginning) the "\def" formatting lines that I pasted. 
</details>

<!--------------------------------------
   NUCLEAR OPTION 
--------------------------------------->
<details>
<summary><b>NUCLEAR OPTION</b> <i>[when nothing else works]</i></summary>
If you just cannot get the table to look like you want it to look, you can always copy/paste the entire NOTANONbiosketches.tex file that appears in the WorPT subfolder, into your document, and then edit at-will.  Some of the WorPT files involve complicated LaTeX code, so be sure that you have a good mastery of LaTeX and know what you are doing before implementing this option!
</details>
