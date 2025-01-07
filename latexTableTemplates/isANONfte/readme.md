<b>NOTANONfte</b> is a table of project tasks, organized under task categories, as specified by the TASKS page in the
WorPT spreadsheet. The task lead and team members assisting with each task are specified as well. No
level-of-effort information is given in this table, only tasks and assignments to illustrate team member involvement. 

<font size="3">WorPT table example: <b>NOTANONfte</b></font>
<br>
<img src="https://lh3.googleusercontent.com/d/1RcQEyCVExdw0WQEikF9MGwOT_K0MQ9CR" width=40%>
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
\include{do_NOT_manually_edit/table_NOTANONfte}   % reset/define parameters used for this file
% NOTE: replace do_NOT_manually_edit if not correct folder name
    
<mark>% Put customizations for NOTANONfte HERE</mark>

\begin{NOTANONfte}
<mark>\caption{Details of work efforts per member to be funded for the present proposal; {\color{red}Detailed responsibilities, tied to tasks and science goals, are provided in Sec.\,\ref{Subsec:tmeline}.}}
\label{tab:isANONfte}</mark>
</code></pre>
</li>
<li><b>Customize appearance</b> [<i>do as many times as needed</i>]
The default table appearance is already optimized, minimizing the need to change table properties such as column widths. However, if you do find the need to make such changes, as well as changes to other properties such as column alignment, colors, font styles, you will need to copy/paste and then edit some additional formatting lines into your document. Specifically: 
<ol>
<li>COPY any or all lines in the code block below that are related to the formatting parameter that you want to edit. The lines below show default values. You will edit those values to make desired changes.</li>
<li>PASTE the copied lines into your document at the "% Put customizations for NOTANONfte HERE" line in the code that you copy/pasted in Step 2. Most importantly, the desired formatting lines should be pasted somewhere <b>between</b> the \include{do_NOT_manually_edit/table_NOTANONfte} and \begin{NOTANONfte} lines. </li>
<li>EDIT the pasted lines in your document, as desired. Some examples are given at the bottom of this page.</li>
NOTE: you can PICK AND CHOOSE the lines you want to paste into your document; you do not have to copy/paste all of the beow lines!
</ol>
<b>Fix the table number if it is showing a wrong number, by adding or subtracting whatever correction is needed.</b>
The default typically works well because the table + longtable combination causes the counter to overcount by one, so -1 performs the appropriate correction.  But ocassionally, the counter gets screwed up and needs manual intervention, so here's how to apply a correction:
<pre><code>
\def\TaskAddCounter{<mark>-1</mark>}        % corrects table number messed up by table,longtable combination)
</code></pre>
<b>The most likely table property that you might want to control is compactness, which can be adjusted by one or more of the following.</b> Highlights indicate what can be edited:
<pre><code>
\def\SpaceBetweenRows{<mark>1.0</mark>}               % vertical compactness of rows
\def\SpaceBetweenColumns{<mark>5pt</mark>}            % spacing between columns
</code></pre>
<b>The below are aesthetic preferences of the column headers.</b> Highlights indicate what can be edited:
<pre><code>
\def\NameLabelBoldface#1{<mark>\textbf</mark>{#1}}      % boldface "Name" column label
\def\RoleLabelBoldface#1{<mark>\textbf</mark>{#1}}      % boldface "Role" column label
\def\CommitmentLabelBoldface#1{<mark>\textbf</mark>{#1}}% boldface "Commitment (FTE)" column label
\def\YearLabelBoldface#1{<mark>\textbf</mark>{#1}}      % boldface "Y1", "Y2", ...  column labels
\def\TotalLabelBoldface#1{<mark>\textbf</mark>{#1}}     % boldface "Total" column label
</code></pre>
<b>The below are aesthetic preferences of the colorized banners separating the categories.</b> Highlights indicate what can be edited:
<pre><code>
\def\SectionBannerColor{<mark>Blue</mark>}              % color of banners separating the 3 sections 
\def\SectionBannerFontColor{<mark>White</mark>}         % font color of banners separating the 3 sections 
\def\SectionBannerBoldface#1{<mark>\textbf</mark>{#1}}  % boldface text in banners separating the 3 sections
</code></pre>
<b>The below are aesthetic preferences of the totals that are summarized at the bottom of each category.</b> Highlights indicate what can be edited:
<pre><code>
\def\TotalWorkEffortBoldface#1{<mark>\textbf</mark>{#1}}% boldface text in "Total .... Work Effort" line at section end
\def\TotalWorkEffortFontColor{<mark>Blue</mark>}        % font color of "Total ... Work Effort" line at section end
</code></pre>

<b>The below table preamble gives you considerably MORE control over table layout than just changing parameter values.</b>
Copy/paste the below if you want to do things like remove or add vertical lines or change a column from left-alignment to center-aligned, for example. You can replace the \TaskWidth and other parameters with hard-coded numbers if desired, and change the "l" (left-align) to other alignment modes. You can change anything that is in highlight. Things that should NOT be changed (otherwise, the LaTeX will break) are the "T" variable and number of columns. 
<pre><code>
\newcolumntype{T}{
  {<mark>|l|</mark>*{\\LastYearPlusOne}{<mark>c|</mark>}}
}
</code></pre> 
</li>
<li><b>Examples</b>
The below is an example of how one can change the appearance of the table within a LaTeX document. After copy/pasting the code to incorporate the table into my document, I decided I wanted to turn the top blue header to green, and the gray shading to yellow shading (resulting in a hideous color scheme, by the way!). I copy/pasted the lines relevant to these formats. Here's what my LaTeX document looks like:  
<pre><code>
\include{do_NOT_manually_edit/NOTANONfte}
% Put customizations for NOTANONfte HERE
                                              
\def\BannerColor{Green}                   % Color of the top "Travel Cost Details" banner
\def\PerTripShadingColor{yellow}           % Shading color of "per trip" columns
\def\PerTripShadingTransparency{0.65}    % Shading transparency for "per trip" colunns; transparent(1.0) - opaque(0.0)

\begin{NOTANONfte}
\caption{}
\label{tab:NOTANONfte}
\end{NOTANONfte}
</code></pre>
NOTE: To return to default values, all I have to do is comment-out (put a "%" at the line's beginning) the "\def" formatting lines that I pasted. 
</li>

<li><b>NUCLEAR OPTION:</b>
If you just cannot get the table to look like you want it to look, you can always copy/paste the entire table_NOTANONfte.tex file that appears in the WorPT subfolder, into your document, and then edit at-will.  Some of the WorPT files involve complicated LaTeX code, so be sure that you have a good mastery of LaTeX and know what you are doing before implementing this option!
</li>
</ol>
