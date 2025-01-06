<b>NOTANONtasks</b> is a table of project tasks, organized under task categories, as specified by the TASKS page in the
WorPT spreadsheet. The task lead and team members assisting with each task are specified as well. No
level-of-effort information is given in this table, only tasks and assignments to illustrate team member involvement. 

<font size="3">WorPT table example: <b>NOTANONtasks</b></font>
<br>
<img src="https://lh3.googleusercontent.com/d/12BO4XZpEwodyHwtDSvcrKBhmCwkxysLS" width=60%>
<hr>
<b>HOW TO USE:</b>
<ol>
<li><b>Special WorPT Packages</b> [<i>one-time-only task</i>] Copy/paste the special packages in preamble of your document, if you haven't done so previously. (see https://github.com/pmarcum/WorPT-Work-Plan-Tool-4-proposals/blob/main/WorPTpackages for more info).</li>
<li><b>How To Put File Contents Into Your Document</b> [<i>do once for inclusion of this file</i>]
These lines will render a table with minimal effort on your part.
<ol>
<li>COPY the lines in the code block below, then</li>
<li>PASTE into your document WHERE you want the content to appear, then</li>
<li>MODIFY the editable lines you just pasted in your document as needed. The editable lines are: the caption, the table label, turning the landscape mode on/off, and inclusion of additional customizations at the designated line (see next step for more details). </li>
</ol>
<pre><code>
\include{\WorPTfolder/mainBody}
%\LandScapetrue                        % uncomment for landscape table
% Put customizations for NOTANONtasks HERE
\begin{NOTANONtasks}
\caption{\normalsize\textbf{Task Management and Team Responsibilities}:\\
The tasks ({\color{red}gray} headers) and sub-tasks (left), with specific assignments for the roles of task lead (middle) and expertise / analysis assistance (right).} \label{tab:NOTANONtasks}
\end{NOTANONtasks}
</code></pre>
NOTE: You need to copy/paste ALL these lines into your document to render the LaTeX as intended. You <b>may</b> delete the lines starting with "%" (e.g., the commented-out lines) if you do not want them in your document, but the remaining lines need to be copy/pasted verbatim. 
</li>
<li><b>Customize appearance</b> [<i>do as many times as needed</i>]
You can change column widths, column alignment, colors, font style using additional lines that are copy/pasted into your document. Specifically: 
<ol>
<li>COPY any or all lines in the code block below that are related to the formatting parameter that you want to edit. The lines below show default values. You will edit those values to make desired changes.</li>
<li>PASTE the copied lines into your document at the "% Put customizations for NOTANONtasks HERE" line in the code that you copy/pasted in Step 2. Most importantly, the desired formatting lines should be pasted somewhere <b>between</b> the \include{\WorPTfolder/mainBody} and \begin{NOTANONtasks} lines. </li>
<li>EDIT the pasted lines in your document, as desired. Some examples are given at the bottom of this page.</li>
NOTE: you can PICK AND CHOOSE the lines you want to paste into your document; you do not have to copy/paste all of the beow lines!
</ol>
<b>The below lines are what you will most likely need to copy/paste, to get your column widths just right:</b>
<pre><code>
\def\TaskWidth{3.9in}            % width of leftmost ("Tasks") column
\def\LeadWidth{1.2in}            % width of middle ("Lead") column
\def\ExpertiseWidth{1.8in}       % width of rightmost ("Expertise") column
\LandScapefalse                  % uncomment for landscape table
</code></pre>
<b>The below lines might be useful - they adjust the table compactness:</b>
<pre><code>
\def\SpaceBetweenRows{1}         % vertical compactness of rows
\def\SpaceBetweenColumns{1pt}    % spacing between columns (bigger value=wider column margin)
</code></pre>
<b>The below can nudge the table to the left (increase value) or right (decrease value)</b>
<pre><code>
\def\WideTable{1.2\textwidth}    % bigger value=nudge table to left
</code></pre>
    
<b>The below are asethetic preferences only, like color and font style</b>
<pre><code>
\def\HeaderColor{Blue}           % column heading color
\def\LabelColor{White}           % column heading font color
\def\LabelBoldface#1{\textbf{#1}}% boldface column labels
\def\SectionColor{gray!40}       % category label colors
\def\TaskColor{Black}            % category label font color
\def\TaskBoldface#1{\textbf{#1}} % boldface task category labels
\def\VerticalLineColor{gray!40}  % color of line between "Lead" and "Expertise"
</code></pre>

<b>The below table preamble gives you considerably MORE control over table layout than just changing parameter values.</b>
Copy/paste the below if you want to do things like remove or add vertical lines or change a column from left-alignment to center-aligned, for example. You can replace the \TaskWidth and other parameters with hard-coded numbers if desired, and change the "p" to other alignment modes. Things that should NOT be changed (otherwise, the LaTeX will break) are the "T" variable and number of columns. 
<pre><code>
\newcolumntype{T}{
  |p{\TaskWidth}||                                 % title column
  p{\LeadWidth}!{\color{\VerticalLineColor}\vrule} % line bet Lead/Expertise% timeline columns
  p{\ExpertiseWidth}|                              % Expertise column
}
</code></pre> 
</li>

<li><b>Examples</b>
The below is an example of how one can change the appearance of the table within a LaTeX document. After copy/pasting the code to incorporate the table into my document, and then deciding that my task titles were too long to fit with the table in portrait mode, I uncommented the landscape flag and copy/pasted the 2 formatting lines that let me make the "Tasks" and "Expertise" columns wider (My team members have long last names, requiring a wider column than the default). I also slightly altered the caption to be appropriate to my proposal. The result?  A landscape-mode table that allows each task to appear in a single table row without spilling over into the next line, which is my preferred way to present these tables for easiest viewing. Here is a peek at what my LaTeX document looks like:  
<pre><code>
\include{do_NOT_manually_edit/NOTANONtasks}
\LandScapetrue                % uncomment for landscape table

\def\TaskWidth{5.4in}          % width of leftmost ("Tasks") column
\def\ExpertiseWidth{1.8in}     % width of rightmost ("Expertise") column

\begin{NOTANONtasks}
\caption{\normalsize\textbf{Task Management and Team Responsibilities}:\\
The tasks ({\color{red}gray} headers) and sub-tasks (left), with specific assignments for the roles of task lead (middle) and expertise / analysis assistance (right). See a more detailed description of these roles in the Project Management section.}
\label{tab:NOTANONtasks}
\end{NOTANONtasks}
</code></pre>
NOTE: To return to default values, all I have to do is comment-out (put a "%" at the line's beginning) the "\def" formatting lines that I pasted. 
</li>

<li><b>NUCLEAR OPTION:</b>
If you just cannot get the table to look like you want it to look, you can always copy/paste the entire table_NOTANONtasks.tex file that appears in the do_NOT_manually_edit folder, into your document, and then edit at-will.  Some of the WorPT files involve complicated LaTeX code, so be sure that you have a good mastery of LaTeX and know what you are doing before implementing this option!
</li>
</ol>
