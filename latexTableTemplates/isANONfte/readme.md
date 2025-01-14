<!--------------------------------------
   SCREEN SHOT
--------------------------------------->
<table>
<tr>
<td>
<font size="3"><b>isANONfte</b></font>
<br>
<img src="https://lh3.googleusercontent.com/d/1RcQEyCVExdw0WQEikF9MGwOT_K0MQ9CR" width=70%>
</td>
<td>
<details>
<summary><b>isANONfte</b> (description)</summary>
<b>isANONfte</b> shows the involved work effort, split out by year and by team member, and including work effort that is both covered by this proposal's budget as well as efforts unfunded by this proposal. The team members are identified only through their roles (PI, co-I, etc.) on the project. 
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
Refer to <b>Customizations</b> section below to add personal preferences in the gap between \expinput and \begin{isANONfte} lines below.

</ol>
   
<pre><code>
%:::::::::::::::::::: start isANONfte ::::::::::::::::::::::
\expinput{<mark>do_NOT_manually_edit</mark>/isANONfte}   % reset file parameters

\begin{isANONfte}
<mark>\caption{Details of work efforts per member to be funded for the present proposal; {\color{red}Detailed responsibilities, tied to tasks and science goals, are provided in Sec.\,\ref{Subsec:tmeline}.}}</mark>
<mark>\label{tab:isANONfte}</mark>
\end{isANONfte}
%::::::::::::::::::::: end isANONfte :::::::::::::::::::::::
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
<li>PASTE the copied lines into your document into the gap <b>between</b> the \expinput and \begin{isANONfte} lines. </li>
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
<td><b>Table number additive correction</b></td>
<td>
The default typically works well (an overcount is caused by table + longtable combination).<br>
But if counter gets screwed up and needs manual intervention, use below to apply a correction:
<pre><code>
\def\TaskAddCounter{<mark>-1</mark>}    % additive correction to table number
</code></pre>
<details>
<summary>reference image</summary>
<img src="https://lh3.googleusercontent.com/d/1iwFp24onzfQsG_goNJ1ytCKsUOT91Cc7" width=50%>
</details>
</td>
</tr>

<tr>
<td><b>Table compactness</b></td>
<td><pre><code>
\def\SpaceBetweenRows{<mark>1</mark>}      % vertical compactness of rows
\def\SpaceBetweenColumns{<mark>1pt</mark>} % bigger = wider spacing between columns
</code></pre>
<details>
<summary>reference image</summary>
<img src="https://lh3.googleusercontent.com/d/1czlAoAQEGa5Hfh1XPlDfgt9ndY0uuui0" width=50%>
</details>
</td>
</tr>

<tr>
<td><b>Column label color and font style</b></td>
<td>
For fontstyle changes, the "\textbf" can be changed to "\emph" for italics, or can<br>
be turned into plain test by removing the "\textbf", eg {{#1}}
<pre><code>
\def\RoleLabelFontstyle#1{<mark>\textbf</mark>{#1}}      % boldface "Role" column label
\def\CommitmentLabelFontstyle#1{<mark>\textbf</mark>{#1}}% boldface "Commitment (FTE)" column label
\def\YearLabelFontstyle#1{<mark>\textbf</mark>{#1}}      % boldface "Y1", "Y2", ...  column labels
\def\TotalLabelFontstyle#1{<mark>\textbf</mark>{#1}}     % boldface "Total" column label
</code></pre>
<details>
<summary>reference image</summary>
<img src="https://lh3.googleusercontent.com/d/12PIlxAVTwR_CvY8ilfmyMFF4oq2az77s" width=50%>
</details>
</td>
</tr>

<tr>
<td><b>Color and font style of category banners</b></td>
<td><pre><code>
\def\SectionBannerColor{<mark>Blue</mark>}              % color of banners separating the 3 sections 
\def\SectionBannerFontColor{<mark>White</mark>}         % font color of banners separating the 3 sections 
\def\SectionBannerFontstyle#1{<mark>\textbf</mark>{#1}}  % boldface text in banners separating the 3 sections
\def\FteFundedBannerText{<mark>Work Efforts Funded By This Proposal</mark>}
\def\FteUnfundedBannerText{<mark>Work Efforts Proposed but NOT Funded By This Proposal</mark>}
\def\FteBothBannerText{<mark>Total Work Efforts Proposed (Funded $+$ Unfunded)</mark>}
</code></pre>
<details>
<summary>reference image</summary>
<img src="https://lh3.googleusercontent.com/d/1IpzNi8JPFHVYT-Li3Vu5UZn3NjKat33x" width=30%>
</details>
</td>
</tr>

<tr>
<td><b>Section summary labelling</b></td>
<td><pre><code>
\def\FteFundedSummaryText{<mark>Total Funded Work Effort</mark>}
\def\FteUnfundedSummaryText{<mark>Total Unfunded Work Effort</mark>}
\def\FteBothSummaryText{<mark>Total Funded $+$ Unfunded Work Effort</mark>}
\def\TotalWorkEffortFontstyle#1{<mark>\textbf</mark>{#1}}% boldface text in "Total .... Work Effort" line at section end
\def\TotalWorkEffortFontColor{<mark>Blue</mark>}        % font color of "Total ... Work Effort" line at section end
</code></pre>
<details>
<summary>reference image</summary>
<img src="https://lh3.googleusercontent.com/d/1IX0Elqi8nXv7uDAzVOJxf6FMVCfOAEMt" width=60%>
</details>
</td>
</tr>

<tr>
<td><b>Table preamble - full control!</b></td>
<td>
Use table preamble for more control over table layout (removing/adding vertical lines, changing column alignment, etc).<br>
Copy/paste the ENTIRE below code in order to change default table preamble.<br>
<u>IMPORTANT</u> Most of table preamble can be changed EXCEPT <i>do <b>NOT</b> change "T" and \LastYearPlusOne variables, and preserve the number of columns</i>
(eg, make sure that any 'l' and 'c' that is removed is replaced by another alignment code).  
<pre><code>
\newcolumntype{T}{
  <mark>|l|</mark>*{\LastYearPlusOne}<mark>{c|}</mark>
}
</code></pre></td>
</table>
</details>

<!--------------------------------------
   EXAMPLES 
--------------------------------------->
<details>
<summary><b>Examples</b></summary>
The below is an example of how one can change the appearance of the table within a LaTeX document. After copy/pasting the code to incorporate the table into my document, I decided I wanted to turn the top blue header to green, and the gray shading to yellow shading (resulting in a hideous color scheme, by the way!). I copy/pasted the lines relevant to these formats. Here's what my LaTeX document looks like:  

<!--     INSERT IMAGE -->

NOTE: To return to default values, all I have to do is comment-out (put a "%" at the line's beginning) the "\def" formatting lines that I pasted. 
</details>

<!--------------------------------------
   NUCLEAR OPTION 
--------------------------------------->
<details>
<summary><b>NUCLEAR OPTION</b> <i>[when nothing else works]</i></summary>
If you just cannot get the table to look like you want it to look, you can always copy/paste the entire isANONfte.tex file that appears in the WorPT subfolder, into your document, and then edit at-will.  Some of the WorPT files involve complicated LaTeX code, so be sure that you have a good mastery of LaTeX and know what you are doing before implementing this option!
</details>
