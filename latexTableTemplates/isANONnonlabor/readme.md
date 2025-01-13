<!--------------------------------------
   SCREEN SHOT
--------------------------------------->
<table>
<tr>
<td>
<font size="3"><b>isANONnonlabor</b></font>
<br>
<img src="https://lh3.googleusercontent.com/d/1qunfPtaL4IOkVOadEu2DLIWkCDcZjGSG" width=70%>
</td>
<td>
<details>
<summary><b>isANONnonlabor</b> (description)</summary>
<b>isANONnonlabor</b> is a table of budget items that include everything except work-effort.  Items such as publication costs, equipment, computers, etc. are included in this table.  Also, rolled-up lines for domestic and international travel are included in the table automatically through the script. (A detailed break-out of travel expenses is provided in the isANONtravel.tex file).<br>
<i>Red font in WorPT file captions flag words that need to be replaced with valid proposal information.</i>
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
\include{<mark>do_NOT_manually_edit</mark>/isANONnonlabor}   % reset parameters used by file
%            ^^^^ replace do_NOT_manually_edit if not correct folder name
%
<mark>% Put <b>OPTIONAL</b> customizations for isANONnonlabor HERE</mark>
%
\begin{isANONnonlabor}
<mark>\caption{
\normalsize \newline \newline
\textbf{Notes and assumptions}:
\newline \newline
{\color{red} \underline{\scshape{Equipment Costs}}: In Yrs~1-2, we request a total of \$11K for the purchase of a laptop and associated IT equipment to replace the PI's aging laptop (purchased in 2018, well past nominal 4-year refresh cycle at the time of the proposed budget period), ``NASA-tized'' computer equipment (laptops, monitors) for use by the summer interns, and as an ``emergency'' fund, should the Science~PI's $\sim$3-yr old laptop fail or need repair.} 
\newline \newline
\underline{\scshape{Travel}}: refer to Table\,\ref{tab:isANONtravel}. \newline \newline
{\color{red} \underline{\scshape{Publication Costs}}: Our work plan includes the publication of four key manuscripts: (see Table \ref{tab:NOTANONschedule} for details),  but given the student projects, we have budgeted for 8 papers. We request a total of \$2K for publication costs,  using the assumption that the papers will fall between "Tier 1" and "Tier 2" categories as defined in ApJ/AJ guidelines. These fees are included in proposed budget.}
\newline \newline
{\color{red}\underline{\scshape{ Materials and Supplies}}: We request an annually-averaged budget of \$1,125 to cover purchase of disk space to back up our data products and miscellaneous office and IT supplies at PI and Science~PI home institution. The distribution of these funds is top-heavy at the beginning of the grant period, when such supplies will be needed most. The disk size of the data products will be approximately 39~Gb per exposure: four \texttt{float32} 
extensions per CCD, corresponding to the \textbf{(1)} Zodiacal-CIB background, \textbf{(2)} in-field, and \textbf{(3)} out-field stray-light, and \textbf{(4)} thermal emission layers, plus one \texttt{binary} extension for the Solar System object trails (\emph{streak / no streak}), for a total of 18~4096$\times$4096 detector focal plane. Storage of these products will not be required, as they will be immediately produced by the pipeline on a exposure-by-exposure basis. End-to-end simulations shall not exceed 100~Gb, and they will be accessible to the community through a public internet server. Publication~IV will require the analysis of an area equivalent to 32 adjacent field of views, the equivalent of a sector of the \RST/WFI High Latitude Wide Area Survey, which corresponds to 128 exposures. Assuming an average exposure size of 9~Gb, plus $\sim$40~Gb for the background products, we project that we will require $\sim$10--15~Tb of disk space (including backups).}}</mark>
<mark>\label{tab:isANONnonlabor}</mark>
\end{isANONnonlabor}
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
<li>PASTE the copied lines into your document at the "% Put customizations for isANONnonlabor HERE" line in the code that you copy/pasted in Step 2. Most importantly, the desired formatting lines should be pasted somewhere <b>between</b> the \include{do_NOT_manually_edit/isANONnonlabor} and \begin{isANONnonlabor} lines. </li>
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
<td><b>Table compactness</b></td>
<td><pre><code>
\def\SpaceBetweenRows{<mark>1.0</mark>}               % vertical compactness of rows
\def\SpaceBetweenColumns{<mark>5pt</mark>}            % spacing between columns
</code></pre></td>
</tr>

<tr>
<td><b>Color and font style of top-row banner</b></td>
<td>
For fontstyle changes, the "\textbf" can be changed to "\emph" for italics, or can<br>
be turned into plain test by removing the "\textbf", eg {{#1}}
<pre><code>
\def\BannerColor{<mark>Blue</mark>}            % "Equipment, Travel, Supplies, Page Charges" banner color
\def\BannerFontColor{<mark>White</mark>}       % "Equipment, Travel, Supplies, Page Charges" banner font color
\def\BannerFontstyle#1{<mark>\textbf</mark>{#1}}% boldface "Equipment, Travel, Supplies, Page Charges" banner
</code></pre></td>
</tr>

<tr>
<td><b>Column label colors and font styles</b></td>
<td>
For fontstyle changes, the "\textbf" can be changed to "\emph" for italics, or can<br>
be turned into plain test by removing the "\textbf", eg {{#1}}
<pre><code>
\def\CostLabelColor{<mark>Blue</mark>}         % "Cost Category" column label color
\def\ColumnFontstyle#1{<mark>\textbf</mark>{#1}}% boldface "Cost Category", "Y1, Y2, ..." column labels 
\def\YearLabelColor{<mark>Blue</mark>}         % "Y1", "Y2", etc  column label color
\def\TotalLabelColor{<mark>Blue</mark>}        % "Total" column label color
\def\TotalFontstyle#1{<mark>\textbf</mark>{#1}}% boldface "Total ..." column label
</code></pre></td>
</tr>

<tr>
<td><b>Font styles for Major budget item rows</b></td>
<td>
For fontstyle changes, the "\textbf" can be changed to "\emph" for italics, or can<br>
be turned into plain test by removing the "\textbf", eg {{#1}}
<pre><code>
\def\MajorCatFontstyle#1{<mark>\textbf</mark>{#1}}   % boldface budget (excl. domestic, internat'l Travel rows) 
\def\MajorAmountFontstyle#1{<mark>\textbf</mark>{#1}}% boldface budget (excl. Total, domestic, internat'l Travel rows) 
\def\MajorCatTotalFontstyle#1{<mark>\textbf</mark>{#1}} % boldface Total budget (excl. domestic, internat'l Travel rows) 
</code></pre></td>
</tr>

<tr>
<td><b>Font styles for travel sub-category item rows</b></td>
<td>
For fontstyle changes, the "\textbf" can be changed to "\emph" for italics, or can<br>
be turned into plain test by removing the "\textbf", eg {{#1}}
<pre><code>
\def\TravelSubcatFontstyle#1{<mark>\textit</mark>{#1}}       % italicize "domestic", "internat'l" rows 
\def\TravelSubcatAmountFontstyle#1{<mark>\textit</mark>{#1}} % italicize "domestic", "internat'l" Travel values 
\def\TravelSubcatTotalFontstyle#1{<mark>\textit{#1}}  % italicize Total,"Domestic"/"International" Travel sums 
</code></pre></td>
</tr>

<tr>
<td><b>Table preamble - full control!</b></td>
<td>
Use table preamble for more control over table layout (removing/adding vertical lines, changing column alignment, etc).<br>
Copy/paste the ENTIRE below code in order to change default table preamble.<br>
<u>IMPORTANT</u> Most of table preamble can be changed EXCEPT <i>do <b>NOT</b> change "T" and \LastYearPlusOne variables, and preserve the number of columns</i>
(eg, make sure that any 'l' that is removed is replaced by another alignment code).  
<pre><code>
\newcolumntype{T}{
   <mark>|l|</mark>*{\LastYearPlusOne}<mark>{l|}</mark>
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
The below is an example of how one can change the appearance of the table within a LaTeX document. After copy/pasting the code to incorporate the table into my document, I decided I wanted to turn the top blue header to green, and the font to black. I copy/pasted the lines relevant to these formats. Here's what my LaTeX document looks like:  

<!--     INSERT IMAGE -->

NOTE: To return to default values, all I have to do is comment-out (put a "%" at the line's beginning) the "\def" formatting lines that I pasted. 
</details>

<!--------------------------------------
   NUCLEAR OPTION 
--------------------------------------->
<details>
<summary><b>NUCLEAR OPTION</b> <i>[when nothing else works]</i></summary>
If you just cannot get the table to look like you want it to look, you can always copy/paste the entire isANONnonlabor.tex file that appears in the WorPT subfolder, into your document, and then edit at-will.  Some of the WorPT files involve complicated LaTeX code, so be sure that you have a good mastery of LaTeX and know what you are doing before implementing this option!
</details>
