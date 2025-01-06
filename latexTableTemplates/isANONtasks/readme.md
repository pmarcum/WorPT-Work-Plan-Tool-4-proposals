<b>isANONtasks</b> is a table of project tasks, organized under task categories, as specified by the TASKS page in the WorPT spreadsheet. The task lead and team members (identified not by name but by project role) assisting with each task are specified as well. No level-of-effort information is given in this table, only tasks and assignments to illustrate team member involvement, as well as start and finish timeline information for each task.

<font size="3">WorPT table example: <b>isANONtasks</b></font>
<br>
<img src="https://lh3.googleusercontent.com/d/1gfMagfSDmX0lDqzAmel2LCGZTuZUGQ5O" width=60%>
<hr>
<b>HOW TO USE:</b>
<ol>
<li><b>Special WorPT Packages</b> [<i>one-time-only task</i>]Copy/paste the special packages in preamble of your document, if you haven't done so previously. (see https://github.com/pmarcum/WorPT-Work-Plan-Tool-4-proposals/blob/main/WorPTpackages for more info).</li>
<li><mark><b>How To Put File Contents Into Your Document</b></mark> [<i>do once for inclusion of this file</i>] 
<ol>
<li>COPY the lines in the code block below, then</li>
<li>PASTE into your document WHERE you want the content to appear, then</li>
<li>MODIFY the editable lines you just pasted in your document as needed. The lines that may be edited (or even deleted altogether if not wanted) are indicated by highlight below. </li>
</ol>
<pre><code>
\include{do_NOT_manually_edit/table_isANONtasks}  % replace do_NOT_manually_edit if not correct folder name
<mark>% Put customizations for isANONtasks HERE</mark>
\begin{isANONtasks}
<mark>\caption{\textbf{Task Timeline:} Team member roles, rightmost column, are cross-referenced with corresponding names in the non-anonymized personnel and work effort table. {\color{red} \textbf{Paper~1:} Sample and methods for enhancing detectability of  low SB X-ray emission, presentation of emission maps, description of database and pipeline software (which will be released in a public repository at the time of paper submission). \textbf{Paper~2:} Methodologies for measuring the gas halo size and other gas properties, analyisis of the diffuse hot gas halos as functions of galaxy properties (environment, galaxy morphology, stellar mass, and SFR based on \Chandra, \Hubble, and \Spitzer\ observations, and the SED models from the GSWLC; application of multivariate mthods to ``baseline'' the  gas halo sizes (Sect.\,\ref{Sec:Baseline}). \textbf{Note~1:} See Sec.\,\ref{Sec:Sample}.}} \label{tab:isANONtasks}</mark>
\end{isANONtasks}
</code></pre>
</li>
<li><b>Customize appearance</b> [<i>do as many times as needed</i>]
You can change column widths, column alignment, colors, font style using additional lines that are copy/pasted into your document. Specifically: 
<ol>
<li>COPY any or all lines in the code block below that are related to the formatting parameter that you want to edit. The lines below show default values. You will edit those values to make desired changes.</li>
<li>PASTE the copied lines into your document at the "% Put customizations for isANONtasks HERE" line in the code that you copy/pasted in Step 2. Most importantly, the desired formatting lines should be pasted somewhere <b>between</b> the \include{do_NOT_manually_edit/table_isANONtasks} and \begin{isANONtasks} lines. </li>
<li>EDIT the pasted lines in your document, as desired. Some examples are given at the bottom of this page.</li>
NOTE: you can PICK AND CHOOSE the lines you want to paste into your document; you do not have to copy/paste all of the beow lines!
</ol>
<b>The below lines are what you will most likely need to copy/paste, to get your column widths just right. Highlights indicate what can be edited:</b>
<pre><code>
\LandScapetrue                 % uncommented-out appearance in your document will put the table in landscape mode
\def\TaskWidth{<mark>3.7in</mark>}          % width of leftmost ("Tasks") column
\def\LeadWidth{<mark>1.1in</mark>}          % width of middle ("Lead") column
\def\ExpertiseWidth{<mark>1.7in</mark>}     % width of rightmost ("Expertise") column
</code></pre>
<b>Fix the table number if it is showing a wrong number, by adding or subtracting whatever correction is needed.</b>
The default typically works well because the table + longtable combination causes the counter to overcount by one, so -1 performs the appropriate correction.  But ocassionally, the counter gets screwed up and needs manual intervention, so here's how to apply a correction:
<pre><code>
\def\TaskAddCounter{<mark>-1</mark>}        % corrects table number messed up by table,longtable combination)
</code></pre>
<b>The below lines might be useful - they adjust the table compactness:</b>
<pre><code>
\def\SpaceBetweenRows{<mark> 1 </mark>}       % vertical compactness of rows
\def\SpaceBetweenColumns{<mark>1pt</mark>}  % spacing between columns (bigger value=wider column margin)
</code></pre>
<b>The below can nudge the table to the left (increase value) or right (decrease value)</b>
<pre><code>
\def\NudgeTable{<mark>1.2\textwidth</mark>} % bigger values nudge table to left
</code></pre>
    
<b>The below are aesthetic preferences only, like color and font style</b>
<pre><code>
\def\TaskCategoryColor{<mark>Blue</mark>}              % task grouping banner color
\def\TaskCategoryFontColor{<mark>White</mark>}         % task grouping title font color
\def\YearFontColor{<mark>Red</mark>}                   % font color under "Y" (year) columns in Start/Finish
\def\YearQuarterLineColor{<mark>lightgray</mark>}      % vertical line color in year/quarter Start/Finish columns
\def\TaskCategoryFontstyle#1{<mark>\textbf</mark>{#1}} % boldface task grouping title
\def\ColumnLabelFontstyle#1{<mark>\textbf</mark>{#1}}  % boldface all the column headers
</code></pre>

<b>The below table preamble gives you considerably MORE control over table layout than just changing parameter values.</b>
Copy/paste the below if you want to do things like remove or add vertical lines or change a column from left-alignment to center-aligned, for example. You can replace the \TaskWidth and other parameters with hard-coded numbers if desired, and change the "p" to other alignment modes. You can change anything that is in highlight. Things that should NOT be changed (otherwise, the LaTeX will break) are the "T" variable and number of columns. 
<pre><code>
\newcolumntype{T}{
  <mark>|p</mark>{<mark>\TaskWidth</mark>}<mark>||</mark>           % title column
  <mark>c</mark>!{<mark>\color{\YearQuarterLineColor}\vrule</mark>} % Start/year
  <mark>c</mark>!{<mark>\color{\YearQuarterLineColor}\vrule</mark>}!{<mark>\color{\YearQuarterLineColor}\vrule</mark>} % Start/quarter
  <mark>c</mark>!<mark>{\color{\YearQuarterLineColor}\vrule</mark>} % Finish/year
  <mark>c||</mark>                        % Finish/quarter
  <mark>p</mark>{<mark>\LeadWidth</mark>}<mark>!{\color{\YearQuarterLineColor}\vrule}</mark> % Task Lead column
  <mark>p</mark>{<mark>\ExpertiseWidth</mark>}<mark>|</mark>        % Expertise column 
}
</code></pre> 
</li>

<li><b>Examples</b>
The below is an example of how one can change the appearance of the table within a LaTeX document. After copy/pasting the code to incorporate the table into my document, and then deciding that my task titles were too long to fit with the table in portrait mode, I decided I needed to use landscape mode.  I copy/pasted the landscape fla and the 2 formatting lines that control the "Tasks" and "Expertise" column widths. (My team members have long last names, requiring a wider column than the default). I also slightly altered the caption to be appropriate to my proposal. The result?  A landscape-mode table that allows each task to appear in a single table row without spilling over into the next line, which is my preferred way to present these tables for easiest viewing. I also decided I wanted the banners that separate the tasks into groups to just be plain text instead of boldfaced. Here is a peek at what my LaTeX document looks like:  
<pre><code>
\include{do_NOT_manually_edit/isANONtasks}
    
\LandScapetrue                 % puts table in landscape mode
\def\TaskWidth{5.4in}          % width of leftmost ("Tasks") column
\def\ExpertiseWidth{1.8in}     % width of rightmost ("Expertise") column
\def\TaskCategoryFontstyle#1{{#1}} % boldface task grouping title

\begin{isANONtasks}
\caption{\normalsize\textbf{Task Management and Team Responsibilities}:\\\\
The tasks ({\color{red}gray} headers) and sub-tasks (left), with specific assignments for the roles of task lead (middle) and expertise / analysis assistance (right). See a more detailed description of these roles in the Project Management section.}
\label{tab:isANONtasks}
\end{isANONtasks}
</code></pre>
NOTE: To return to default values, all I have to do is comment-out (put a "%" at the line's beginning) the "\def" formatting lines that I pasted. 
</li>

<li><b>NUCLEAR OPTION:</b>
If you just cannot get the table to look like you want it to look, you can always copy/paste the entire table_isANONtasks.tex file that appears in the WorPT subfolder, into your document, and then edit at-will.  Some of the WorPT files involve complicated LaTeX code, so be sure that you have a good mastery of LaTeX and know what you are doing before implementing this option!
</li>
</ol>
