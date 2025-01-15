<!--------------------------------------
   SCREEN SHOT
--------------------------------------->
<table>
<tr>
<td>
<font size="3"><b>isANONtravel</b></font>
<br>
<img src="https://lh3.googleusercontent.com/d/1BZUJ-Wzdl-T8crM779V0AoAxww-myF64" width=60%>
</td>
<td>
<details>
<summary><b>isANONtravel</b> (description)</summary>
<b>isANONtravel</b> is a table of project tasks, organized under task categories, as specified by the TASKS page in the
WorPT spreadsheet. The task lead and team members assisting with each task are specified as well. No
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
<li>MODIFY the editable lines you just pasted in your document as needed. The lines that may be edited (or even deleted altogether if not wanted) are indicated by highlight below. </li><br>
Refer to <b>Customizations</b> section below to add personal preferences in the gap between \expinput and \begin{isANONtravel} lines below.

</ol>
   
<pre><code>
%::::::::::::::::: start isANONtravel ::::::::::::::::::::
\expinput{<mark>do_NOT_manually_edit</mark>/isANONtravel}  % reset file parameters

\begin{isANONtravel}  
<mark>\caption{\normalsize \newline \newline
\textbf{Notes and assumptions}:
\newline \newline
While final destinations are not known at this time, domestic and international costs are estimated based on values taken from NASA Travel Guidebook using historical averages for a \daysPerDomesticTrip-- and \daysPerInternationalTrip--day conference for U.S. and European cities, resp., likely to host topical meetings aligned with the science of the proposed work. Domestic lodging and per diem rates are set by the GSA; international lodging and per diem are set by the Dept. of State (note that M\&IE is included in the per diem values shown here).
\newline \newline \noindent {\color{red} Yrs~1-2 funds will be used to present pre-publication findings at science conferences and potentially to fund trips for collaboration with team members (i.e., NASA/GSFC).}
\newline \newline \underline{\scshape{domestic}}: 
per diem$+$M\&IE, car rental/day at \$\domesticPerDiemDollars\ and \$\domesticGroundTravelDollars, resp.
\newline \newline \underline{\scshape{international}}: 
per diem$+$M\&IE, public transport/day estimated at  \$\internationalPerDiemDollars\ and \$\internationalGroundTravelDollars, resp.
\newline \newline \underline{\scshape{Travel Per Team Member}} 
(summed over \grantYears-year grant):
\newline
\perPersonNumberTripsList\
\newline All travel will be to present science results of this project at conferences and/or visits to home institutions of the team members for in-person collaboration. Note that above values above do not include institutional overhead.}</mark>
<mark>\label{tab:isANONtravel}</mark>
\end{isANONtravel}
%::::::::::::::::::: end isANONtravel ::::::::::::::::::::::
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
<li>PASTE the copied lines into your document into the gap <b>between</b> the \expinput and \begin{isANONtravel} lines. </li>
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
\def\SpaceBetweenRows{<mark>1.0</mark>}    % vertical compactness of rows
\def\SpaceBetweenColumns{<mark>5pt</mark>} % bigger = wider spacing between columns
</code></pre>
<details>
<summary>reference image</summary>
<img src="https://lh3.googleusercontent.com/d/11nB6CliLC7Xj4pYc3E88ZEPDjcskKUj0" width=45%>
</details>
</td>
</tr>

<tr>
<td><b>Top banner color and font style</b></td>
<td><pre><code>
\def\BannerFontstyle#1{<mark>\textbf</mark>{#1}} % Bold-face for top banner "Travel Cost Details
\def\BannerColor{<mark>Blue</mark>}              % Color of the top "Travel Cost Details" banner
\def\BannerFontColor{<mark>White</mark>}         % Font color for top "Travel Cost Details" banner
</code></pre>
<details>
<summary>reference image</summary>
<img src="https://lh3.googleusercontent.com/d/1CB_e_g9cgl-p6bZrXiV2vaYLcRfnBo7A" width=45%>
</details>
</td>
</tr>

<tr>
<td><b>Column color shading</b></td>
<td><pre><code>
\def\PerTripShadingColor{<mark>gray!15</mark>}        % Shading color of "per trip" columns
</code></pre>
<details>
<summary>reference image</summary>
<img src="https://lh3.googleusercontent.com/d/1KABYTWPNODR3-QaHLInz-je8XuhoxTsV" width=45%>
</details>
</td>
</tr>

<tr>
<td><b>Column heading color and font style</b></td>
<td><pre><code>
\def\YearTripsDestLabelFontColor{<mark>Blue</mark>}   % Font color for "Year", "#TRips" and "Dest." column labels
\def\TotalLabelFontColor{<mark>Blue</mark>}           % Font color "Total" column label
\def\TotalLabelFontstyle#1{<mark>\textbf</mark>{#1}}       % Bold-face column label "Total"
\def\PerTripLabelFontColor{<mark>Blue</mark>}         % Font color of column labels for "per trip" section
\def\PerTripLabelFontstyle#1{<mark>\textbf</mark>{#1}}     % Bold-face column labels for "per trip" section
\def\YearTripsDestFontstyle#1{<mark>\textbf</mark>{#1}}% Bold-face "Year", "#Trips", "Dest." labels
\def\YearFontstyle#1{<mark>\textbf</mark>{#1}}        % Bold-face "Yr1", "YR2", etc labels
</code></pre>
<details>
<summary>reference image</summary>
<img src="https://lh3.googleusercontent.com/d/15WoAr8LTBeCeR_K4WR-drOVYS3wUpTTu" width=60%>
</details>
</td>
</tr>

<tr>
<td><b>Table preamble - full control!</b></td>
<td>
Use table preamble for more control over table layout (removing/adding vertical lines, changing column alignment, etc).<br>
Copy/paste the ENTIRE below code in order to change default table preamble.<br>
<u>IMPORTANT</u> Most of table preamble can be changed EXCEPT <i>do <b>NOT</b> change "T" variable, and preserve the number of columns</i>
(eg, make sure that any 'l' or "c" that is removed is replaced by another alignment code). You may retain the parameters below (like \PerTripShadingColor) and define them separately as the above customization options show, or replace them entirely with hard-coded numbers. 
<pre><code>
\newcolumntype{T}{
 <mark>|lcl >{\columncolor{\PerTripShadingColor}[\tabcolsep][\PerTripShadingMargin]}</mark> 
 <mark>l >{\columncolor{\PerTripShadingColor}[\tabcolsep][\PerTripShadingMargin]}</mark> 
 <mark>l >{\columncolor{\PerTripShadingColor}[\tabcolsep][\PerTripShadingMargin]}</mark> 
 <mark>l >{\columncolor{\PerTripShadingColor}[\tabcolsep][\PerTripShadingMargin]}</mark> 
 <mark>l >{\columncolor{\PerTripShadingColor}[\tabcolsep][\PerTripShadingMargin]}</mark> 
 <mark>ll|</mark>
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
The below is an example of how one can change the appearance of the table within a LaTeX document. After copy/pasting the code to incorporate the table into my document, I decided I wanted to turn the top blue header to green, and the gray shading to yellow shading (resulting in a hideous color scheme, by the way!). I copy/pasted the lines relevant to these formats. Here's what my LaTeX document looks like:  

<!--     INSERT IMAGE -->

NOTE: To return to default values, all I have to do is comment-out (put a "%" at the line's beginning) the "\def" formatting lines that I pasted. 
</details>

<!--------------------------------------
   NUCLEAR OPTION 
--------------------------------------->
<details>
<summary><b>NUCLEAR OPTION</b> <i>[when nothing else works]</i></summary>
If you just cannot get the table to look like you want it to look, you can always copy/paste the entire isANONtravel.tex file that appears in the WorPT subfolder, into your document, and then edit at-will.  Some of the WorPT files involve complicated LaTeX code, so be sure that you have a good mastery of LaTeX and know what you are doing before implementing this option!
</details>
