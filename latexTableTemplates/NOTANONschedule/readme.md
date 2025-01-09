<!--------------------------------------
   SCREEN SHOT
--------------------------------------->
<table>
<tr>
<td>
<font size="3">WorPT table example: <b>NOTANONschedule</b></font>
<br>
<img src="https://lh3.googleusercontent.com/d/1rdPPWxa8nlGOFGYbZyQ6Frq9zj01w4Ww" width=50%>
</td>
<td>
<details>
<summary><b>DESCRIPTION</b></summary>
<b>NOTANONschedule</b> is a table of project tasks, organized under task categories, as specified by the TASKS page in the WorPT spreadsheet. The task lead and team members assisting with each task are specified as well. No
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
\newpage                                       % [optional] could instead use \clearpage
\include{do_NOT_manually_edit/NOTANONschedule} % reset file parameters
%            ^^^^ replace do_NOT_manually_edit if not correct folder name

 
<mark>% Put OPTIONAL customizations for NOTANONschedule HERE</mark>

\begin{NOTANONschedule}
<mark>\caption{Resource-loaded project schedule, where: 
{\TotalFteUnfundedHeaderIcon\hspace{-0.3em}$=$\hspace{-0.3em}}Not funded by this grant, {\TotalFteFundedHeaderIcon\hspace{-0.3em}$=$\hspace{-0.3em}}funded by this grant, {\TotalFteSumHeaderIcon\hspace{-0.3em}$=$\hspace{-0.3em}}funded $+$ unfunded; Tasks are listed (left side), with duration of task activity indicated in blue-colored timelines that measure quarter-years (1,2,3,4). Task assignments identify specific team members responsible for implementation with associated work weeks, where color indicates institutional affiliation (blue$=$funded/U.S., black$=$not funded/U.S., red=international). "Total FTE" (right side) are integrated work-weeks converted into FTE per task (1~FTE$=$12~months), displayed as "total",  "unfunded by this grant", and "funded by this grant", resp.  Assignment identities: \RevealIdentities.}
\label{tab:NOTANONschedule}</mark>
\end{NOTANONhst}
</code></pre>

</details>

<!-- - - - - - - - - - - - - - - - - - - - - - - - - - - - 
             Customizations
- - - - - - - - - - - - - - - - - - - - - - - - - - - - -->
<details>
<summary><b>Customize appearance</b> [<i>do as many times as needed</i>]</summary>
You can change column widths, column alignment, colors, font style using additional lines that are copy/pasted into your document. Specifically: 
<ol>
<li>COPY any or all lines in the code block below that are related to the formatting parameter that you want to edit. The lines below show default values. You will edit those values to make desired changes.</li>
<li>PASTE the copied lines into your document at the "% Put OPTIONAL customizations for NOTANONschedule HERE" line in the code that you copy/pasted in Step 2. Most importantly, the desired formatting lines should be pasted somewhere <b>between</b> the \include{do_NOT_manually_edit/table_NOTANONhst} and \begin{NOTANONhst} lines. </li>
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
<td><b>Column width adjustments</b></td>
<td><pre><code>
\def\TitleWidth{<mark>4.1in</mark>}      % Title column width
\def\TimelineWidth{<mark>1ex</mark>}     % skinny timeline columns width
\def\AssignmentsWidth{<mark>24ex</mark>} % Task assignments column width
\def\SumFteWidth{<mark>5ex</mark>}       % Total FTE/Sum column width
\def\UnfundedFteWidth{<mark>5ex</mark>}  % Total FTE/Unfunded column width
\def\FundedFteWidth{<mark>5ex</mark>}    % Total FTE/Funded column width
</code></pre></td>
</tr>

<tr>
<td><b>Column label font adjustments</b></td>
<td><pre><code>
\def\TaskTimelineHeaderFontsize{<mark>\scriptsize</mark>}   % Task Timeline label text size
\def\TaskAssignmentsHeaderFontsize{<mark>\scriptsize</mark>}% Task Assignments label text size
\def\TotalFteHeaderFontsize{<mark>\scriptsize</mark>}       % Totaled FTEs label text size
\def\YearHeaderFontsize{<mark>\scriptsize</mark>}           % "YEAR1", "YEAR2"... label text size
\def\TaskTitleHeaderFontsize{<mark>\normalsize</mark>}      % "TASK TITLES" column label text size
\def\YearSliceHeaderFontsize{<mark>\scriptsize</mark>}      % "1", "2"... year-quarter label text size
\def\IdWksHeaderFontsize{<mark>\scriptsize</mark>}          % "id wks" text size  
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
<td><b>Format preferences for task CATEGORY labels</b></td>
<td>
For fontstyle changes, the "\textbf" can be changed to "\emph" for italics, or can<br>
be turned into plain test by removing the "\textbf" or other formatting. You do 
need to keep the #1 and #2 references. For example, if you just want plain text, you could
redefine as:<br>
\def\TaskCategoryLabel#1#2{{#1}~{#2}}
<pre><code>
\def\TaskCategoryLabel#1#2{          % Task Category label format for row item
  {\normalsize\textbf\scshape{#1}}~{\normalsize\textbf{#2}}}
</code></pre></td>
</tr>

%---- symbol preferences for FTE types (sum, funded, unfunded)
\def\TotalFteSumHeaderIcon{\textbf{\large{$\Sigma$}}} % sigma symbol label size
\def\TotalFteUnfundedHeaderIcon{\noDollarIcon{-0.4}{0.4mm}{0.2}{0.15}} % "no dollar" symbol label size
\def\TotalFteFundedHeaderIcon{\dollarIcon{-0.4}{0.2}{0.015}}% green "dollar" symbol label size


%---- vertical line colors
\def\TimelineVerticalLineColor{lightgray}
\def\TotalFteVerticalLineColor{lightgray}


%--- aesthetic preferences of task CATEGORY label

%--- aesthetic preferences of TASK label
\def\TaskTitleLabel#1#2{                       % Task title format for row item
  ~{\scriptsize{\textbf{\scshape{#1}}}}~{
  \color{mediumelectricblue}{\footnotesize\textbf{#2}}}}

%--- aesthetic preferences of timeline color
\def\TimelineColor{mediumelectricblue}          % Task Timeline cell color

%--- preferences for indicating US vs non-US instutional affiliations and funded vs unfunded team members
\def\FundedUsTeam#1{\small \color{blue}{#1}}    % funded US team members ID, \#weeks format
\def\UnfundedUsTeam#1{\small \color{black}{#1}} % UNfunded US team members ID, \#weeks fomat
\def\InternationalTeam#1{\small \color{red}{#1}}% international team members ID, \#weeks format

%--- preferences for formatting the FTE values in far right columns
\def\FteTotalFormat#1{\small{#1}}               % Total FTE/sum value format
\def\FteUnfundedFormat#1{\small{#1}}            % Total FTE/unfunded value format
\def\FteFundedFormat#1{\small \color{blue}{#1}} % Total FTE/funded value format

%--- Format the identity reveals in the table caption
\def\RevealIdentityFormat#1#2{\textbf{#1}: #2}


<tr>
<td><b>Table preamble - full control!</b></td>
<td>
Use table preamble for more control over table layout (removing/adding vertical lines, changing column alignment, etc).<br>
Copy/paste the ENTIRE below code in order to change default table preamble.<br>
<u>IMPORTANT</u> Most of table preamble can be changed EXCEPT <i>do <b>NOT</b> change "T" and "L" variables, and preserve the number of columns.</i>
<pre><code>
\newcolumntype{T}{
  |>{\raggedright\arraybackslash}p{\TitleWidth}                  % title column
  *{\NumberYears}{|p{\TimelineWidth}!{\color{\TimelineVerticalLineColor}\vrule}*{\SlicesPerYearMinusTwo}{p{\TimelineWidth}!{\color{\TimelineVerticalLineColor}\vrule}}p{\TimelineWidth}}    % timeline columns
  |>{\raggedright\arraybackslash}p{\AssignmentsWidth}            % task assignment column
  |p{\SumFteWidth}!{\color{\TotalFteVerticalLineColor}\vrule}    % total fte, sum column
  p{\UnfundedFteWidth}!{\color{\TotalFteVerticalLineColor}\vrule}% total fte, unfunded column
  p{\FundedFteWidth}|                                            % total fte, funded column
}
</code></pre>
</td>
</tr>
</table>
</details>

<!--------------------------------------
   EXAMPLES 
--------------------------------------->
<details>
<summary><b>Examples</b></summary>
The below is an example of how one can change the appearance of the table within a LaTeX document. After copy/pasting the code to incorporate the table into my document, and then deciding that my task titles were too long to fit with the table in portrait mode, I decided I needed to use landscape mode.  I copy/pasted the landscape fla and the 2 formatting lines that control the "Tasks" and "Expertise" column widths. (My team members have long last names, requiring a wider column than the default). I also slightly altered the caption to be appropriate to my proposal. The result?  A landscape-mode table that allows each task to appear in a single table row without spilling over into the next line, which is my preferred way to present these tables for easiest viewing. Here is a peek at what my LaTeX document looks like:  
<pre><code>
\include{do_NOT_manually_edit/NOTANONhst}
    
\def\TaskWidth{5.4in}          % width of leftmost ("Tasks") column
\def\ExpertiseWidth{1.8in}     % width of rightmost ("Expertise") column

\begin{NOTANONhst}
\caption{Resource-loaded project schedule, where: 
{\TotalFteUnfundedHeaderIcon\hspace{-0.3em}$=$\hspace{-0.3em}}Not funded by this grant,  
{\TotalFteFundedHeaderIcon\hspace{-0.3em}$=$\hspace{-0.3em}}funded by this grant, 
{\TotalFteSumHeaderIcon\hspace{-0.3em}$=$\hspace{-0.3em}}funded $+$ unfunded; 
Tasks are listed (left side), with duration of task activity indicated in blue-colored timelines that 
measure quarter-years (1,2,3,4). Task assignments identify specific team members responsible for 
implementation with associated work weeks, where color indicates institutional affiliation 
(blue$=$funded/U.S., black$=$not funded/U.S., red=international). "Total FTE" (right side) are integrated 
work-weeks converted into FTE per task (1~FTE$=$12~months), displayed as "total",  "unfunded by this grant", 
and "funded by this grant", resp.  Assignment identities: \RevealIdentities.}
\label{tab:NOTANONschedule} 

\end{NOTANONhst}
</code></pre>
NOTE: To return to default values, all I have to do is comment-out (put a "%" at the line's beginning) the "\def" formatting lines that I pasted. 
</details>

<!--------------------------------------
   NUCLEAR OPTION 
--------------------------------------->
<details>
<summary><b>NUCLEAR OPTION</b> <i>[when nothing else works]</i></summary>
If you just cannot get the table to look like you want it to look, you can always copy/paste the entire table_NOTANONhst.tex file that appears in the WorPT subfolder, into your document, and then edit at-will.  Some of the WorPT files involve complicated LaTeX code, so be sure that you have a good mastery of LaTeX and know what you are doing before implementing this option!
</details>
