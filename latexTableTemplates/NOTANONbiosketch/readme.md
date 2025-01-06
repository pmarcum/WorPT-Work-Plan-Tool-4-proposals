<b>NOTANONbiosketch</b> is a table of project tasks, organized under task categories, as specified by the TASKS page in the
WorPT spreadsheet. The task lead and team members assisting with each task are specified as well. No
level-of-effort information is given in this table, only tasks and assignments to illustrate team member involvement. 

<font size="3">WorPT table example: <b>NOTANONbiosketch</b></font>
<br>
<img src="https://lh3.googleusercontent.com/d/1f3XxoAT5680nxNbcwWk4uifOvXdytuUh" width=40%>
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
\include{\WorPTfolder/mainBody}
<mark>% Put customizations for NOTANONbiosketch HERE</mark>
\begin{NOTANONbiosketch}
<mark>\caption{\normalsize\textbf{Task Management and Team Responsibilities}:\\
The tasks ({\color{red}gray} headers) and sub-tasks (left), with specific assignments for the roles of task lead (middle) and expertise / analysis assistance (right).} \label{tab:NOTANONbiosketch}</mark>
\end{NOTANONbiosketch}
</code></pre>
</li>
<li><b>Customize appearance</b> [<i>do as many times as needed</i>]
You can change column widths, column alignment, colors, font style using additional lines that are copy/pasted into your document. Specifically: 
<ol>
<li>COPY any or all lines in the code block below that are related to the formatting parameter that you want to edit. The lines below show default values. You will edit those values to make desired changes.</li>
<li>PASTE the copied lines into your document at the "% Put customizations for NOTANONbiosketch HERE" line in the code that you copy/pasted in Step 2. Most importantly, the desired formatting lines should be pasted somewhere <b>between</b> the \include{\WorPTfolder/mainBody} and \begin{NOTANONbiosketch} lines. </li>
<li>EDIT the pasted lines in your document, as desired. Some examples are given at the bottom of this page.</li>
NOTE: you can PICK AND CHOOSE the lines you want to paste into your document; you do not have to copy/paste all of the beow lines!
</ol>
<b>The below lines are what you will most likely need to copy/paste, to get your column widths just right. Highlights indicate what can be edited:</b>
<pre><code>
\LandScapetrue                   % uncommented-out appearance in your document will put the table in landscape mode
\def\TaskWidth{<mark>3.9in</mark>}            % width of leftmost ("Tasks") column
\def\LeadWidth{<mark>1.2in</mark>}            % width of middle ("Lead") column
\def\ExpertiseWidth{<mark>1.8in</mark>}       % width of rightmost ("Expertise") column
</code></pre>
<b>Fix the table number if it is showing a wrong number, by adding or subtracting whatever correction is needed.</b>
The default typically works well because the table + longtable combination causes the counter to overcount by one, so -1 performs the appropriate correction.  But ocassionally, the counter gets screwed up and needs manual intervention, so here's how to apply a correction:
<pre><code>
\def\TaskAddCounter{<mark>-1</mark>}          % corrects table number messed up by table,longtable combination)
</code></pre>
<b>The below lines might be useful - they adjust the table compactness:</b>
<pre><code>
\def\SpaceBetweenRows{<mark>1</mark>}         % vertical compactness of rows
\def\SpaceBetweenColumns{<mark>1pt</mark>}    % spacing between columns (bigger value=wider column margin)
</code></pre>
<b>The below can nudge the table to the left (increase value) or right (decrease value)</b>
<pre><code>
\def\NudgeTable{<mark>1.2\textwidth</mark>}    % bigger values nudge table to left
</code></pre>
    
<b>The below are aesthetic preferences only, like color and font style</b>
<pre><code>
\def\HeaderColor{<mark>Blue</mark>}           % column heading color
\def\HeaderFontColor{<mark>White</mark>}           % column heading font color
\def\HeaderBoldface#1{<mark>\textbf</mark>{#1}}% boldface column heading labels; change "\textbf" to "\emph" or whatever
\def\SectionColor{<mark>gray!40</mark>}       % category dection label colors
\def\SectionFontColor{<mark>Black</mark>}            % category section label font color
\def\SectionBoldface#1{<mark>\textbf</mark>{#1}} % boldface category section labels; change "\textbf" to "\emph" or whatever
\def\VerticalLineColor{<mark>gray!40</mark>}  % color of line between "Lead" and "Expertise"
</code></pre>

<b>The below table preamble gives you considerably MORE control over table layout than just changing parameter values.</b>
Copy/paste the below if you want to do things like remove or add vertical lines or change a column from left-alignment to center-aligned, for example. You can replace the \TaskWidth and other parameters with hard-coded numbers if desired, and change the "p" to other alignment modes. You can change anything that is in highlight. Things that should NOT be changed (otherwise, the LaTeX will break) are the "T" variable and number of columns. 
<pre><code>
\newcolumntype{T}{
  <mark>|p</mark>{<mark>\TaskWidth</mark>}<mark>||</mark>                                 % title column
  <mark>p</mark>{<mark>\LeadWidth</mark>}<mark>!{\color{\VerticalLineColor}\vrule}</mark> % line bet Lead/Expertise
  <mark>p</mark>{<mark>\ExpertiseWidth</mark>}<mark>|</mark>                              % Expertise column
}
</code></pre> 
</li>

<li><b>Examples</b>
The below is an example of how one can change the appearance of the table within a LaTeX document. After copy/pasting the code to incorporate the table into my document, and then deciding that my task titles were too long to fit with the table in portrait mode, I decided I needed to use landscape mode.  I copy/pasted the landscape fla and the 2 formatting lines that control the "Tasks" and "Expertise" column widths. (My team members have long last names, requiring a wider column than the default). I also slightly altered the caption to be appropriate to my proposal. The result?  A landscape-mode table that allows each task to appear in a single table row without spilling over into the next line, which is my preferred way to present these tables for easiest viewing. Here is a peek at what my LaTeX document looks like:  
<pre><code>
\include{\WorPTfolder/NOTANONbiosketch}
    
\LandScapetrue                 % puts table in landscape mode
\def\TaskWidth{5.4in}          % width of leftmost ("Tasks") column
\def\ExpertiseWidth{1.8in}     % width of rightmost ("Expertise") column

\begin{NOTANONbiosketch}
\caption{\normalsize\textbf{Task Management and Team Responsibilities}:\\\\
The tasks ({\color{red}gray} headers) and sub-tasks (left), with specific assignments for the roles of task lead (middle) and expertise / analysis assistance (right). See a more detailed description of these roles in the Project Management section.}
\label{tab:NOTANONbiosketch}
\end{NOTANONbiosketch}
</code></pre>
NOTE: To return to default values, all I have to do is comment-out (put a "%" at the line's beginning) the "\def" formatting lines that I pasted. 
</li>

<li><b>NUCLEAR OPTION:</b>
If you just cannot get the table to look like you want it to look, you can always copy/paste the entire table_NOTANONbiosketch file that appears in the WorPT subfolder, into your document, and then edit at-will.  Some of the WorPT files involve complicated LaTeX code, so be sure that you have a good mastery of LaTeX and know what you are doing before implementing this option!
</li>
</ol>
