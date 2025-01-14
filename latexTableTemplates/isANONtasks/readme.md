<!--------------------------------------
   SCREEN SHOT
--------------------------------------->
<table>
<tr>
<td>
<font size="3"><b>isANONtasks</b></font>
<br>
<img src="https://lh3.googleusercontent.com/d/1gfMagfSDmX0lDqzAmel2LCGZTuZUGQ5O" width=80%>
</td>
<td>
<details>
<summary><b>isANONtasks</b> (description)</summary>
<b>isANONtasks</b> is a table of project tasks, organized under task categories, as specified by the TASKS page in the WorPT spreadsheet. The task lead and team members (identified not by name but by project role) assisting with each task are specified as well. No level-of-effort information is given in this table, only tasks and assignments to illustrate team member involvement, as well as start and finish timeline information for each task.
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
\include{<mark>do_NOT_manually_edit</mark>/isANONtasks}  % reset file parameters
%            ^^^^ replace do_NOT_manually_edit if not correct folder name
%
<mark>% Put <b>OPTIONAL</b> customizations for isANONtasks HERE</mark>
%
\begin{isANONtasks}
<mark>\caption{\textbf{Task Timeline:} Team member roles, rightmost column, are cross-referenced with corresponding names in the non-anonymized personnel and work effort table. {\color{red} \textbf{Paper~1:} Sample and methods for enhancing detectability of  low SB X-ray emission, presentation of emission maps, description of database and pipeline software (which will be released in a public repository at the time of paper submission). \textbf{Paper~2:} Methodologies for measuring the gas halo size and other gas properties, analyisis of the diffuse hot gas halos as functions of galaxy properties (environment, galaxy morphology, stellar mass, and SFR) based on \Chandra, \Hubble, and \Spitzer\ observations, and the SED models from the GSWLC; application of multivariate mthods to ``baseline'' the  gas halo sizes (Sect.\,\ref{Sec:Baseline}). \textbf{Note~1:} See Sec.\,\ref{Sec:Sample}.}}</mark>
<mark>\label{tab:isANONtasks}</mark>
\end{isANONtasks}
</code></pre>

</details>

<!-- - - - - - - - - - - - - - - - - - - - - - - - - - - - 
             Customizations
- - - - - - - - - - - - - - - - - - - - - - - - - - - - -->
<details>
<summary><b>Customize appearance</b> [<i>do as many times as needed</i>]</summary>
The default table appearance is already optimized, minimizing the need to change table properties such as column widths. However, if you do find the need to make such changes, as well as changes to other properties such as column alignment, colors, font styles, you will need to copy/paste and then edit some additional formatting lines into your document. Specifically:
<ol>
<li>COPY any or all lines in the code block below that are related to the formatting parameter that you want to edit. The lines below show default values. You will edit those values to make desired changes.</li>
<li>PASTE the copied lines into your document at the "% Put customizations for isANONtasks HERE" line in the code that you copy/pasted in Step 2. Most importantly, the desired formatting lines should be pasted somewhere <b>between</b> the \include{do_NOT_manually_edit/isANONtasks} and \begin{isANONtasks} lines. </li>
<li>EDIT the pasted lines in your document, as desired.</li>
NOTE: THe lines are grouped into categories to help you locate what you need. You can PICK AND CHOOSE the lines you want to paste into your document; you do not have to copy/paste all of the lines below (unless noted) and do not have to copy all lines within a group.<br>
<i>Highlights indicate what parts of the commands can be edited without breaking your LaTeX code.</i><br>
You can just comment out your added lines and recompile the document, if you want to return to default values.
</ol>

<!-- . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                              Options   
<!-- . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . -->
<table>
 
<tr>
<td><b>Table orientation</b></td>
<td><pre><code>
\LandScapetrue          % will put the table in landscape mode
</code></pre>
<details>
<summary>reference image</summary>
<img src="https://lh3.googleusercontent.com/d/1vMs3teKHoqZGHGqHZj4HrtaZZp9Xq0Xa" width=20%>
</details>
</td>
</tr>

<tr>
<td><b>Column width adjustments</b></td>
<td><pre><code>
\def\TaskWidth{<mark>3.4in</mark>}      % width of leftmost ("Tasks") column
\def\StartFinishWidth{<mark>0.2in</mark>}           % width of start/finish columns
\def\LeadWidth{<mark>0.5in</mark>}      % width of middle ("Lead") column
\def\ExpertiseWidth{<mark>1.5in</mark>} % width of rightmost ("Expertise") column
</code></pre>
<details>
<summary>reference image</summary>
<img src="https://lh3.googleusercontent.com/d/13oCZxeIfopxwB6SfXjmThW4JepSNconJ" width=60%>
</details>
</td>
</tr>

<tr>
<td><b>Table number additive correction</b></td>
<td>
The default typically works well (an overcount is caused by table + longtable combination).<br>
But if counter gets screwed up and needs manual intervention, use below to apply a correction:
<pre><code>
\def\TaskAddCounter{<mark>-1</mark>}    % additive correction to table number
</code></pre>
<details>
<summary>reference image</summary>
<img src="https://lh3.googleusercontent.com/d/1Qm9oKnrRSBDZQLlinY6nyBQjGY7M2pcX" width=60%>
</details>
</td>
</tr>

<tr>
<td><b>Table compactness</b></td>
<td><pre><code>
\def\SpaceBetweenRows{<mark>0.87</mark>}    % vertical compactness of rows
\def\SpaceBetweenColumns{<mark>2pt</mark>} % bigger = wider spacing between columns
</code></pre>
<details>
<summary>reference image</summary>
<img src="https://lh3.googleusercontent.com/d/16uvtXkaEDCZRso5eqzBA3Y3NKo4rjphn" width=60%>
</details>
</td>
</tr>

<tr>
<td><b>Nudge table to left or right</b></td>
<td><pre><code>
\def\NudgeTable{<mark>1.2\textwidth</mark>} % larger value nudges table to left
</code></pre>
<details>
<summary>reference image</summary>
<img src="https://lh3.googleusercontent.com/d/1sTVcig_jiHo8iuKm6R_71L1Voxptdtjr" width=60%>
</details>
</td>
</tr>
    
<tr>
<td><b>Color and font style of category banners</b></td>
<td><pre><code>
\def\SectionColor{<mark>Blue</mark>}              % category section label colors
\def\SectionFontColor{<mark>White</mark>}         % category title font color
\def\SectionFontstyle#1{<mark>\textbf</mark>{#1}} % boldface category title
</code></pre>
<details>
<summary>reference image</summary>
<img src="https://lh3.googleusercontent.com/d/1gxJcyUbm5iVLsKrsxrynn-wuqp7-YgnU" width=60%>
</details>
</td>
</tr>

<tr>
<td><b>Color and font style of column headers</b></td>
<td><pre><code>
\def\ColumnLabelFontstyle#1{<mark>\textbf</mark>{#1}}  % boldface all the column headers
\def\YearFontColor{<mark>Red</mark>}                   % font color under "Y" (year) columns in Start/Finish
</code></pre>
<details>
<summary>reference image</summary>
<img src="https://lh3.googleusercontent.com/d/1FyRgEblao5yAiiuGxC78IHeV6m9k3843" width=60%>
</details>
</td>
</tr>

<tr>
<td><b>Color of faint vertical line</b></td>
<td><pre><code>
\def\YearQuarterLineColor{<mark>lightgray</mark>}      % vertical line color in year/quarter Start/Finish columns
</code></pre>
<details>
<summary>reference image</summary>
<img src="https://lh3.googleusercontent.com/d/1LHdvupXYjQmpvncz-UxbGuyjAjdidLnY" width=60%>
</details>
</td>
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
  <mark>|p{\TaskWidth}||</mark>                        % title column
  <mark>c!{\color{\YearQuarterLineColor}\vrule}</mark> % Start/year
  <mark>c!{\color{\YearQuarterLineColor}\vrule}!{\color{\YearQuarterLineColor}\vrule}</mark> % Start/quarter
  <mark>c!{\color{\YearQuarterLineColor}\vrule}</mark> % Finish/year
  <mark>c||</mark>                                     % Finish/quarter
  <mark>p{\LeadWidth}!{\color{\YearQuarterLineColor}\vrule}</mark> % Task Lead column
  <mark>p{\ExpertiseWidth}|</mark>                     % Expertise column 
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
The below is an example of how one can change the appearance of the table within a LaTeX document. After copy/pasting the code to incorporate the table into my document, and then deciding that my task titles were too long to fit with the table in portrait mode, I decided I needed to use landscape mode.  I copy/pasted the landscape fla and the 2 formatting lines that control the "Tasks" and "Expertise" column widths. (My team members have long last names, requiring a wider column than the default). I also altered the caption to be appropriate to my proposal (e.g., changed the red font that signaled words that needed to be adapted). The result?  A landscape-mode table that allows each task to appear in a single table row without spilling over into the next line, which is my preferred way to present these tables for easiest viewing. I also decided I wanted the banners that separate the tasks into groups to just be plain text instead of boldfaced. I also wanted to left-align the Start and Finish columns. Here is a peek at what my LaTeX document looks like:  

<!--     INSERT IMAGE -->

NOTE: To return to default values, all I have to do is comment-out (put a "%" at the line's beginning) the "\def" formatting lines that I pasted. 
</details>

<!--------------------------------------
   NUCLEAR OPTION 
--------------------------------------->
<details>
<summary><b>NUCLEAR OPTION</b> <i>[when nothing else works]</i></summary>
If you just cannot get the table to look like you want it to look, you can always copy/paste the entire isANONtasks.tex file that appears in the WorPT subfolder, into your document, and then edit at-will.  Some of the WorPT files involve complicated LaTeX code, so be sure that you have a good mastery of LaTeX and know what you are doing before implementing this option!
</details>
