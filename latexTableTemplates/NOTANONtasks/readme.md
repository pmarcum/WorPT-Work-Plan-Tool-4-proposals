<!--------------------------------------
   SCREEN SHOT
--------------------------------------->
<table>
<tr>
<td>
<font size="3"><b>NOTANONtasks</b></font>
<br>
<img src="https://lh3.googleusercontent.com/d/12BO4XZpEwodyHwtDSvcrKBhmCwkxysLS" width=70%>
</td>
<td>
<details>
<summary><b>NOTANONtasks</b> (description)</summary>
<b>NOTANONtasks</b> is a table of project tasks, organized under task categories, as specified by the TASKS page in the
WorPT spreadsheet. The task lead and team members assisting with each task are specified as well. No
level-of-effort information is given in this table, only tasks and assignments to illustrate team member involvement. 
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
<li>MODIFY the editable lines you just pasted in your document as needed. The lines that may be edited (or even deleted altogether if not wanted) are indicated by highlight below. </li>
</ol>
    
<pre><code>
\newpage                                          % [optional] (could instead use \clearpage, or comment out)
\include{<mark>do_NOT_manually_edit</mark>/NOTANONtasks} % reset file parameters
%            ^^^^ replace do_NOT_manually_edit if not correct folder name
%
<mark>% Put <b>OPTIONAL</b> customizations for NOTANONtasks HERE</mark>
%
\begin{NOTANONtasks}
<mark>\caption{\normalsize\textbf{Task Management and Team Responsibilities}:\\
The tasks ({\color{red}gray} headers) and sub-tasks (left), with specific assignments for the roles of task lead (middle) and expertise / analysis assistance (right).} \label{tab:NOTANONtasks}</mark>
\end{NOTANONtasks}
</code></pre>

</details>

<!-- - - - - - - - - - - - - - - - - - - - - - - - - - - - 
             Customizations
- - - - - - - - - - - - - - - - - - - - - - - - - - - - -->
<details>
<summary><b>Customize appearance</b> [<i>do as many times as needed</i>]</summary 
You can change column widths, column alignment, colors, font style using additional lines that are copy/pasted into your document. Specifically: 
<ol>
<li>COPY any or all lines in the code block below that are related to the formatting parameter that you want to edit. The lines below show default values. You will edit those values to make desired changes.</li>
<li>PASTE the copied lines into your document at the "% Put customizations for NOTANONtasks HERE" line in the code that you copy/pasted in Step 2. Most importantly, the desired formatting lines should be pasted somewhere <b>between</b> the \include{do_NOT_manually_edit/NOTANONtasks} and \begin{NOTANONtasks} lines. </li>
<li>EDIT the pasted lines in your document, as desired. Some examples are given at the bottom of this page.</li>
NOTE: you can PICK AND CHOOSE the lines you want to paste into your document; you do not have to copy/paste all of the beow lines!
</ol>

<!-- . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                              Options   
<!-- . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . -->
<table>

<tr>
<td><b>Table orientation</b></td>
<td><pre><code>
\LandScapetrue          % will put the table in landscape mode
</code></pre></td>
</tr>

<tr>
<td><b>Column width adjustments</b></td>
<td><pre><code>
\def\TaskWidth{<mark>3.9in</mark>}            % leftmost ("Tasks") column width
\def\LeadWidth{<mark>1.2in</mark>}            % middle ("Lead") column width
\def\ExpertiseWidth{<mark>1.8in</mark>}       % rightmost ("Expertise") column width
</code></pre></td>
</tr>

<tr>
<td><b>Table number additive correction</b></td>
<td>
The default typically works well (an overcount is caused by table + longtable combination).<br>
But if counter gets screwed up and needs manual intervention, use below to apply a correction:
<pre><code>
\def\TaskAddCounter{<mark>-1</mark>}    % additive correction to table number
</code></pre></td>
</tr>

<tr>
<td><b>Table compactness</b></td>
<td><pre><code>
\def\SpaceBetweenRows{<mark>0.8</mark>}    % vertical compactness of rows
\def\SpaceBetweenColumns{<mark>1pt</mark>} % bigger = wider spacing between columns
</code></pre></td>
</tr>

<tr>
<td><b>Nudge table to left or right</b></td>
<td><pre><code>
\def\NudgeTable{<mark>1.5\textwidth</mark>} % larger value nudges table to left
</code></pre></td>
</tr>
   
<tr>
<td><b>Column label color and font style</b></td>
<td>
For fontstyle changes, the "\textbf" can be changed to "\emph" for italics, or can
be turned into plain test by removing the "\textbf", eg {{#1}}
<pre><code>
\def\HeaderColor{<mark>Blue</mark>}            % column heading color
\def\HeaderFontColor{<mark>White</mark>}       % column heading font color
\def\HeaderFontstyle#1{<mark>\textbf</mark>{#1}}% boldface column heading labels
</code></pre></td>
</tr>

<tr>
<td><b>Color and font style of category banners</b></td>
<td><pre><code>
\def\SectionColor{<mark>gray!40</mark>}       % category section label colors
\def\SectionFontColor{<mark>Black</mark>}     % category section label font color
\def\SectionFontstyle#1{<mark>\textbf</mark>{#1}} % boldface category section labels
</code></pre></td>
</tr>

<tr>
<td><b>Color of faint vertical line</b></td>
<td><pre><code>
\def\VerticalLineColor{<mark>gray!40</mark>}  % color of line between "Lead" and "Expertise"
</code></pre></td>
</tr>

<tr>
<td><b>Table preamble - full control!</b></td>
<td>
Use table preamble for more control over table layout (removing/adding vertical lines, changing column alignment, etc).<br>
Copy/paste the ENTIRE below code in order to change default table preamble.<br>
<u>IMPORTANT</u> Most of table preamble can be changed EXCEPT <i>do <b>NOT</b> change "T" variable, and preserve the number of columns</i>
(eg, make sure that any 'p' that is removed is replaced by another alignment code). You may retain the parameters below (like \TaskWidth) and
define them separately as the above customization options show, or replace them entirely with hard-coded numbers. 
   
<pre><code>
\newcolumntype{T}{
  <mark>|p</mark>{<mark>\TaskWidth</mark>}<mark>||</mark>                                 % title column
  <mark>p</mark>{<mark>\LeadWidth</mark>}<mark>!{\color{\VerticalLineColor}\vrule}</mark> % task lead column
  <mark>p</mark>{<mark>\ExpertiseWidth</mark>}<mark>|</mark>                              % expertise column
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
The below is an example of how one can change the appearance of the table within a LaTeX document. After copy/pasting the code to incorporate the table into my document, and then deciding that my task titles were too long to fit with the table in portrait mode, I decided I needed to use landscape mode.  I copy/pasted the landscape fla and the 2 formatting lines that control the "Tasks" and "Expertise" column widths. (My team members have long last names, requiring a wider column than the default). I also slightly altered the caption to be appropriate to my proposal. The result?  A landscape-mode table that allows each task to appear in a single table row without spilling over into the next line, which is my preferred way to present these tables for easiest viewing. Here is a peek at what my LaTeX document looks like:  

<!--     INSERT IMAGE -->

NOTE: To return to default values, all I have to do is comment-out (put a "%" at the line's beginning) the "\def" formatting lines that I pasted. 
</details>

<!--------------------------------------
   NUCLEAR OPTION 
--------------------------------------->
<details>
<summary><b>NUCLEAR OPTION</b> <i>[when nothing else works]</i></summary>
If you just cannot get the table to look like you want it to look, you can always copy/paste the entire NOTANONtasks.tex file that appears in the WorPT subfolder, into your document, and then edit at-will.  Some of the WorPT files involve complicated LaTeX code, so be sure that you have a good mastery of LaTeX and know what you are doing before implementing this option!
</details>
