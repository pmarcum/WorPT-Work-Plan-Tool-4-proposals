<!--------------------------------------
   SCREEN SHOT
--------------------------------------->
<table>
<tr>
<td>
<font size="3"><b>NOTANONschedule</b></font>
<br>
<img src="https://lh3.googleusercontent.com/d/1rdPPWxa8nlGOFGYbZyQ6Frq9zj01w4Ww" width=75%>
</td>
<td>
<details>
<summary><b>NOTANONschedule</b> (description)</summary>
<b>NOTANONschedule</b> is resource-loaded project schedule showing project tasks, milestones with associated timelines, and team member roles. The table provides the work effort involved for each task, divided into effort directly funded by this proposal, unfunded, and total.  Institutional affiliation (U.S. or international) is also indicated.  The information in this table is taken primarily from the TASKS page in the WorPT spreadsheet.
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
\newpage                                       % [optional] (could instead use \clearpage, or comment out)
\include{<mark>do_NOT_manually_edit</mark>/NOTANONschedule} % reset file parameters
%            ^^^^ replace do_NOT_manually_edit if not correct folder name
%
<mark>% Put <b>OPTIONAL</b> customizations for NOTANONschedule HERE</mark>
%
\begin{NOTANONschedule}
<mark>\caption{Resource-loaded project schedule, where: 
{\TotalFteUnfundedHeaderIcon\hspace{-0.3em}$=$\hspace{-0.3em}}Not funded by this grant, {\TotalFteFundedHeaderIcon\hspace{-0.3em}$=$\hspace{-0.3em}}funded by this grant, {\TotalFteSumHeaderIcon\hspace{-0.3em}$=$\hspace{-0.3em}}funded $+$ unfunded; Tasks are listed (left side), with duration of task activity indicated in blue-colored timelines that measure quarter-years (1,2,3,4). Task assignments identify specific team members responsible for implementation with associated work weeks, where color indicates institutional affiliation (blue$=$funded/U.S., black$=$not funded/U.S., red=international). "Total FTE" (right side) are integrated work-weeks converted into FTE per task (1~FTE$=$12~months), displayed as "total",  "unfunded by this grant", and "funded by this grant", resp.  Assignment identities: \RevealIdentities.}
\label{tab:NOTANONschedule}</mark>
\end{NOTANONschedule}
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
<li>PASTE the copied lines into your document at the "% Put OPTIONAL customizations for NOTANONschedule HERE" line in the code that you copy/pasted in Step 2. Most importantly, the desired formatting lines should be pasted somewhere <b>between</b> the \include{do_NOT_manually_edit/NOTANONschedule} and \begin{NOTANONschedule} lines. </li>
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
</code></pre>
<details>
<summary>reference image</summary>
<img src="https://lh3.googleusercontent.com/d/1dXDf4XkJcMxWQ1Q5zYmiN1Z0QKpHpFLV" width=70%>
</details>
</td>
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
</code></pre>
<details>
<summary>reference image</summary>
<img src="https://lh3.googleusercontent.com/d/1Og1zQoUqQuLJB8sbMlIiaDNviE-RBah6" width=70%>
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
<img src="https://lh3.googleusercontent.com/d/1mYVKCIdWEPoyEQuEr2SYSAsr5-vGl48k" width=30%>
</details>
</td>
</tr>

<tr>
<td><b>Table compactness</b></td>
<td><pre><code>
\def\SpaceBetweenRows{<mark>0.8</mark>}    % vertical compactness of rows
\def\SpaceBetweenColumns{<mark>1pt</mark>} % bigger = wider spacing between columns
</code></pre>
<details>
<summary>reference image</summary>
<img src="https://lh3.googleusercontent.com/d/1wgKhN-aCTVc2Vi6bJ8FAyoZrK3f8SNfA" width=30%>
</details></td>
</tr>

<tr>
<td><b>Nudge table to left or right</b></td>
<td><pre><code>
\def\NudgeTable{<mark>1.5\textwidth</mark>} % larger value nudges table to left
</code></pre>
<details>
<summary>reference image</summary>
<img src="https://lh3.googleusercontent.com/d/1sgYYaDtI7YJF_sMnKDn7jXHWfZtgNBJX" width=30%>
</details>
</td>
</tr>

<tr>
<td><b>CATEGORY, TASK label row entry formatting</b></td>
<td>
For fontstyle changes, the "\textbf" can be changed to "\emph" for italics, or can<br>
be turned into plain test by removing the "\textbf" or other formatting. You do 
need to keep the #1 and #2 references. For example, if you just want plain text, you could
redefine as:<br>
\def\TaskCategoryLabel#1#2{{#1}~{#2}}
<pre><code>
\def\TaskCategoryLabel#1#2{{<mark>\normalsize\textbf\scshape</mark>{#1}}~
   {<mark>\normalsize\textbf</mark>{#2}}}                               % Category label
\def\TaskTitleLabel#1#2{~{<mark>\scriptsize{\textbf{\scshape</mark>{#1}}}}~
   {<mark>\color{mediumelectricblue}{\footnotesize\textbf</mark>{#2}}}} % Task title format for row item
</code></pre>
<details>
<summary>reference image</summary>
<img src="https://lh3.googleusercontent.com/d/1FptrYPilkvMpYVCh0EHQX5cKxFiZXUFh" width=30%>
</details>
</td>
</tr>

<tr>
<td><b>Vertical line colors</b></td>
<td><pre><code>
\def\TimelineVerticalLineColor{<mark>lightgray</mark>} % vertical line in timeline section
\def\TotalFteVerticalLineColor{<mark>lightgray</mark>} % vertical line in total fte section
</code></pre>
<details>
<summary>reference image</summary>
<img src="https://lh3.googleusercontent.com/d/1AewnKa1OXlrgT4bNIqy3JrVWkqW4lcYR" width=30%>
</details></td>
</tr>

<tr>
<td><b>Color of task timelines</b></td>
<td><pre><code>
\def\TimelineColor{<mark>mediumelectricblue</mark>} % Task Timeline cell color
</code></pre>
<details>
<summary>reference image</summary>
<img src="https://lh3.googleusercontent.com/d/12H_J3b7oNhnd9ZDHivqEkQ2gdAJl8hWV" width=30%>
</details></td>
</tr>

<tr>
<td><b>Institutional affiliation and funded vs unfunded formatting</b></td>
<td><pre><code>
\def\FundedUsTeam#1{<mark>\small \color{blue}</mark>{#1}}    % funded US team members ID, \#weeks format
\def\UnfundedUsTeam#1{<mark>\small \color{black}</mark>{#1}} % UNfunded US team members ID, \#weeks fomat
\def\InternationalTeam#1{<mark>\small \color{red}</mark>{#1}}% international team members ID, \#weeks format
</code></pre>
<details>
<summary>reference image</summary>
<img src="https://lh3.googleusercontent.com/d/1cio03IIIDCGoOO5_4htjm2LV6q0JmEe4" width=30%>
</details>
</td>
</tr>

<tr>
<td><b>FTE values in rightmost columns</b></td>
<td><pre><code>
\def\FteTotalFormat#1{<mark>\small</mark>{#1}}               % Total FTE/sum value format
\def\FteUnfundedFormat#1{<mark>\small</mark>{#1}}            % Total FTE/unfunded value format
\def\FteFundedFormat#1{<mark>\small \color{blue}</mark>{#1}} % Total FTE/funded value format
</code></pre>
<details>
<summary>reference image</summary>
<img src="https://lh3.googleusercontent.com/d/1aqfgM6GA6TCNEcAKQ-pyegkXKijkH889" width=30%>
</details>
</td>
</tr>

<tr>
<td><b>Team member identify table caption formatting</b></td>
<td><pre><code>
\def\RevealIdentityFormat#1#2{<mark>\textbf</mark>{#1}<mark>: </mark>#2} % \#1=ID, \#2=Name
</code></pre>
<details>
<summary>reference image</summary>
<img src="https://lh3.googleusercontent.com/d/1nrSrK1mSC0hJRuNJs6Vxf4jZlveQ48BL" width=30%>
</details>
</td>
</tr>

<tr>
<td><b>Symbol preferences for FTE types</b></td>
<td><pre><code>
\def\TotalFteSumHeaderIcon{<mark>\textbf{\large{$\Sigma$}}</mark>}       % FTE sum symbol
\def\TotalFteUnfundedHeaderIcon{<mark>\noDollarIcon{-0.4}{0.4mm}{0.2}{0.15}</mark>} % "FTE unfunded symbol
\def\TotalFteFundedHeaderIcon{<mark>\dollarIcon{-0.4}{0.2}{0.015}</mark>}% FTE funded symbol
</code></pre>
<details>
<summary>reference image</summary>
<img src="https://lh3.googleusercontent.com/d/1kdg5LRFovZQT9oI7B-eGPh5RJ9KARgmg" width=30%>
</details>
</td>
</tr>

<tr>
<td><b>Delimiter of team members under TASK ASSIGNMENTS</b></td>
<td><pre><code>
\def\TaskAssignmentDelimiter{;\hspace{3pt}} % delimiter used in TASK ASSIGNMENTS
</code></pre>
<details>
<summary>reference image</summary>
<img src="https://lh3.googleusercontent.com/d/1AwZgBxEbQJB6sw5vg68fL2uH0bFsj5Ht" width=30%>
</details>
</td>
</tr>

<tr>
<td><b>Table preamble - full control!</b></td>
<td>
Use table preamble for more control over table layout (removing/adding vertical lines, changing column alignment, etc).<br>
Copy/paste the ENTIRE below code in order to change default table preamble.<br>
<u>IMPORTANT</u> Most of table preamble can be changed EXCEPT <i>do <b>NOT</b> change "T", \NumberYears and \SlicesPerYearMinusTwo variables, and preserve the number of columns (eg, make sure that any 'p' that is removed is replaced by another alignment code). The helper definitions of "L", "V" and "W" may be changed or removed.</i>
<pre><code>
%--- table preamble definition bundled into the "T" variable
<mark>\newcolumntype{L}[1]{>{\raggedright\arraybackslash}p{#1}}</mark>      % title, assignment columns
<mark>\newcolumntype{V}{!{\color{\TimelineVerticalLineColor}\vrule}}</mark> % vertical lines in timeline
<mark>\newcolumntype{W}{!{\color{\TotalFteVerticalLineColor}\vrule}}</mark> % vertical lines in FTE
%
\newcolumntype{T}{
<mark>|L{\TitleWidth}</mark>         % title column
*{\NumberYears}{        % timeline columns
<mark>|p{\TimelineWidth}V</mark>*{\SlicesPerYearMinusTwo}<mark>{p{\TimelineWidth}V}p{\TimelineWidth}}</mark> 
<mark>|L{\AssignmentsWidth}</mark>   % task assignment column
<mark>|p{\SumFteWidth}W</mark>       % total fte, sum column
<mark>p{\UnfundedFteWidth}W</mark>   % total fte, unfunded column
<mark>p{\FundedFteWidth}|</mark>     % total fte, funded column
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
If you just cannot get the table to look like you want it to look, you can always copy/paste the entire NOTANONschedule.tex file that appears in the WorPT subfolder, into your document, and then edit at-will.  Some of the WorPT files involve complicated LaTeX code, so be sure that you have a good mastery of LaTeX and know what you are doing before implementing this option!
</details>
