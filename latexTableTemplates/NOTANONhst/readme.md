<!--------------------------------------
   SCREEN SHOT
--------------------------------------->
<table>
<tr>
<td>
<font size="3"><b>NOTANONhst</b></font>
<br>
<img src="https://lh3.googleusercontent.com/d/1OpijauwkFzgEorqyUsArZlkZz6ZcB__d" width=70%>
</td>
<td>
<details>
<summary><b>NOTANONhst</b> (description)</summary>
<b>NOTANONhst</b> is a tabulated summary of team member roles, following the format for HST Phase II proposals.  The table lists each team member, their relationship to the project (PI, co-I, etc.), their institutional affiliation and whether or not the institution is U.S.-based, and a brief narrative summary of their role on the project. The table also indicates if the team member is funded or unfunded through the proposal, and what their total level of work effort (in FTE) is.
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
Refer to <b>Customizations</b> section below to add personal preferences in the gap between \expinput and \begin{NOTANONhst} lines below.
</ol>
   
<pre><code>
%:::::::::::::::::::: start NOTANONhst ::::::::::::::::::::::
\expinput{<mark>do_NOT_manually_edit</mark>/NOTANONhst} % reset file parameters
\def\ProgramID{<mark>HST-xx-xxxxx (Cycle XX)</mark>} % <mark><b>fill in details</b></mark>

\begin{NOTANONhst}
<mark>\caption{\textbf{Work Effort for All Members}\hspace{1em} Team members, identified by their name and role in the proposed project, are listed with their institutional affiliation and position, with a "F" or "US" indicating foreign or U.S. institution. A brief narrative of their role in the project is given.  A 'Y' or 'N' indicates if the person is funded by the proposed budget or not, respectively.  The total work-effort of the team member, summed over full life of the proposed  project, is in the rightmost column (multiply displayed FTE value by 12 to get work effort in number of months units).}
\label{tab:NOTANONhst}</mark>
\end{NOTANONhst}
%::::::::::::::::::::: end NOTANONhst :::::::::::::::::::::::
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
<li>PASTE the copied lines into your document into the gap <b>between</b> the \def\ProgramID and \begin{NOTANONhst} lines. </li>
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
\def\ContributorWidth{<mark>1.8in</mark>}      % Contributor column width
\def\PositionWidth{<mark>1.3in</mark>}         % Position column width
\def\RoleWidth{<mark>2.5in</mark>}             % Role column width
\def\FundedMemberWidth{<mark>0.22in</mark>}    % Funded(?) column width
\def\FteWidth{<mark>0.42in</mark>}             % FTE column width
</code></pre>
<details>
<summary>reference image</summary>
<img src="https://lh3.googleusercontent.com/d/1VFoxre2-539OyEXfklTvudu-PYBlPuaJ" width=70%>
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
<img src="https://lh3.googleusercontent.com/d/1XhVrw4lR70_WbosdIZ7x-mowtJRTPVqs" width=50%>
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
<img src="https://lh3.googleusercontent.com/d/16KK8AuYbxc5C0dy9qPh2Pazoq_XdEWD2" width=50%>
</details>
</td>
</tr>

<tr>
<td><b>Table number additive correction</b></td>
<td>
The default typically works well (an overcount is caused by table + longtable combination). But if counter gets screwed up and needs manual intervention, use below to apply a correction:
<pre><code>
\def\TaskAddCounter{<mark>-1</mark>}    % additive correction to table number
</code></pre>
<details>
<summary>reference image</summary>
<img src="https://lh3.googleusercontent.com/d/1Vc29554V1Sny5-E8O-nm3IiZ1-NnGEQf" width=50%>
</details>
</td>
</tr>

<tr>
<td><b>Column label color and font style</b></td>
<td>
For fontstyle changes, the "\textbf" can be changed to "\emph" for italics, or can be turned into plain test by removing the "\textbf", eg {{#1}}
<pre><code>
\def\HeaderColor{<mark>Blue</mark>}             % column heading color
\def\LabelColor{<mark>White</mark>}             % column heading font color
\def\LabelFontstyle#1{<mark>\textbf</mark>{#1}} % boldface column label
\def\VerticalLineColor{<mark>lightgray</mark>}  % color of vertical lines
</code></pre>
<details>
<summary>reference image</summary>
<img src="https://lh3.googleusercontent.com/d/1VlOwoxQeP8kprw-Ua_XleCuhklszXV7Z" width=50%>
</details>
</td>
</tr>

<tr>
<td><b>Table preamble - full control!</b></td>
<td>
Use table preamble for more control over table layout (removing/adding vertical lines, changing column alignment, etc). Copy/paste the ENTIRE below code in order to change default table preamble.<br>
<u>IMPORTANT</u> Most of table preamble can be changed EXCEPT <i>do <b>NOT</b> change "T" variable, and preserve the number of columns</i> (eg, make sure that any 'p' that is removed is replaced by another alignment code). You may retain the parameters below (like \ContributorWidth) and define them separately as the above customization options show, or replace them entirely with hard-coded numbers. You can also change the column user-definition of "L" if desired.
<pre><code>
% define column type to help readability of table preamble
<mark>\newcolumntype{L}[1]{>{\raggedright\let\newline\\\arraybackslash\hspace{0pt}}p{#1}}</mark>
%
\newcolumntype{T}{                                       % start of table preamble
<mark>|L{\ContributorWidth}!{\color{\VerticalLineColor}\vrule}</mark> % Contributor
<mark>L{\PositionWidth}!{\color{\VerticalLineColor}\vrule}</mark>     % Position
<mark>L{\RoleWidth}!{\color{\VerticalLineColor}\vrule}</mark>         % Role
<mark>p{\FundedMemberWidth}!{\color{\VerticalLineColor}\vrule}</mark> % Funded(?)
<mark>p{\FteWidth}|</mark>                                            % FTE
}                                                        % end of table preamble
</code></pre></td>
</tr>

</table>
</details>

<!--------------------------------------
   EXAMPLES 
--------------------------------------->
<details>
<summary><b>Examples</b></summary>
The below is an example of how one can change the appearance of the table within a LaTeX document. After copy/pasting the code to incorporate the table into my 

 <img src="https://lh3.googleusercontent.com/d/1QOff63_b8AUEFpRMKUlaGK0LcEz3NvCK" width=50%>


   
<!-- INSERT IMAGE HERE -->
NOTE: To return to default values, all I have to do is comment-out (put a "%" at the line's beginning) the "\def" formatting lines that I pasted. 
</details>

<!--------------------------------------
   NUCLEAR OPTION 
--------------------------------------->
<details>
<summary><b>NUCLEAR OPTION</b> <i>[when nothing else works]</i></summary>
If you just cannot get the table to look like you want it to look, you can always copy/paste the entire NOTANONhst.tex file that appears in the WorPT subfolder, into your document, and then edit at-will.  Some of the WorPT files involve complicated LaTeX code, so be sure that you have a good mastery of LaTeX and know what you are doing before implementing this option!
</details>
