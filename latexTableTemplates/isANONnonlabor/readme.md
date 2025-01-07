<b>isANONnonlabor</b> is a table of project tasks, organized under task categories, as specified by the TASKS page in the
WorPT spreadsheet. The task lead and team members assisting with each task are specified as well. No
level-of-effort information is given in this table, only tasks and assignments to illustrate team member involvement. 

<font size="3">WorPT table example: <b>isANONnonlabor</b></font>
<br>
<img src="https://lh3.googleusercontent.com/d/1qunfPtaL4IOkVOadEu2DLIWkCDcZjGSG" width=60%>
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
\include{do_NOT_manually_edit/table_isANONnonlabor}   % reset/define parameters used for this file
% NOTE: replace do_NOT_manually_edit if not correct folder name
    
<mark>% Put customizations for isANONnonlabor HERE</mark>

\begin{isANONnonlabor}
<mark>\caption{
\normalsize \newline \newline
\textbf{Notes and assumptions}:
\newline \newline
{\color{red} \underline{\scshape{Equipment Costs}}: In Yrs~1-2, we request a total of \\$11K for the purchase of a laptop and associated IT equipment to replace the PI's aging laptop (purchased in 2018, well past nominal 4-year refresh cycle at the time of the proposed budget period), ``NASA-tized'' computer equipment (laptops, monitors) for use by the summer interns, and as an ``emergency'' fund, should the Science~PI's $\sim$3-yr old laptop fail or need repair.} 
\newline \newline
\underline{\scshape{Travel}}: refer to Table\,\ref{tab:isANONtravel}. \newline \newline
{\color{red} \underline{\scshape{Publication Costs}}: Our work plan includes the publication of four key manuscripts: (see Table \ref{tab:NOTANONschedule} for details),  but given the student projects, we have budgeted for 8 papers. We request a total of \\$2K for publication costs,  using the assumption that the papers will fall between "Tier 1" and "Tier 2" categories as defined in ApJ/AJ guidelines. These fees are included in proposed budget.}
\newline \newline
{\color{red}\underline{\scshape{ Materials and Supplies}}: We request an annually-averaged budget of \\$1,125 to cover purchase of disk space to back up our data products and miscellaneous office and IT supplies at PI and Science-PI home institution. The distribution of these funds is top-heavy at the beginning of the grant period, when such supplies will be needed most. The disk size of the data products will be approximately ~39~Gb per exposure: four \\texttt{float32} 
extensions per CCD, corresponding to the \textbf{(1)} Zodiacal-CIB background, \\textbf{(2)} in-field, and \\textbf{(3)} out-field stray-light, and \textbf{(4)} thermal emission layers, plus one \texttt{binary} extension for the Solar System object trails (\emph{streak / no streak}), for a total of 18~4096$\times$4096 detector focal plane. Storage of these products will not be required, as they will be immediately produced by the pipeline on a exposure-by-exposure basis. End-to-end simulations shall not exceed 100~Gb, and they will be accessible to the community through a public internet server. Publication~IV will require the analysis of an area equivalent to 32 adjacent field of views, the equivalent of a sector of the \RST/WFI High Latitude Wide Area Survey, which corresponds to 128 exposures. Assuming an average exposure size of 9~Gb, plus $\sim$40~Gb for the background products, we project that we will require $\sim$10--15~Tb of disk space (including backups).}}
\label{tab:isANONnonlabor}</mark>
\end{isANONnonlabor}
</code></pre>
</li>
<li><b>Customize appearance</b> [<i>do as many times as needed</i>]
The default table appearance is already optimized, minimizing the need to change table properties such as column widths. However, if you do find the need to make such changes, as well as changes to other properties such as column alignment, colors, font styles, you will need to copy/paste and then edit some additional formatting lines into your document. Specifically: 
<ol>
<li>COPY any or all lines in the code block below that are related to the formatting parameter that you want to edit. The lines below show default values. You will edit those values to make desired changes.</li>
<li>PASTE the copied lines into your document at the "% Put customizations for isANONnonlabor HERE" line in the code that you copy/pasted in Step 2. Most importantly, the desired formatting lines should be pasted somewhere <b>between</b> the \include{do_NOT_manually_edit/table_isANONnonlabor} and \begin{isANONnonlabor} lines. </li>
<li>EDIT the pasted lines in your document, as desired. Some examples are given at the bottom of this page.</li>
NOTE: you can PICK AND CHOOSE the lines you want to paste into your document; you do not have to copy/paste all of the beow lines!
</ol>
<b>The most likely table property that you might want to control is compactness, which can be adjusted by one or more of the following.</b> Highlights indicate what can be edited:
<pre><code>
\def\SpaceBetweenRows{<mark>1.0</mark>}               % vertical compactness of rows
\def\SpaceBetweenColumns{<mark>5pt</mark>}            % spacing between columns
</code></pre>
<b>The below are aesthetic preferences only, like color and font style.</b> Highlights indicate what can be edited:
<pre><code>
\def\BannerFontstyle#1{<mark>\textbf</mark>{#1}}      % Bold-face for top banner "Travel Cost Details
\def\BannerColor{<mark>Blue</mark>}                   % Color of the top "Travel Cost Details" banner
\def\BannerFontColor{<mark>White</mark>}              % Font color for top "Travel Cost Details" banner
\def\PerTripShadingColor{<mark>gray</mark>}           % Shading color of "per trip" columns
\def\PerTripShadingTransparency{<mark>0.85</mark>}    % Shading transparency for "per trip" colunns; transparent(1.0) - opaque(0.0)
\def\PerTripShadingMargin{<mark>7pt</mark>}           % Margin width to right of each shaded "per trip" column (prevents white vertical line)
\def\YearTripsDestLabelFontColor{<mark>Blue</mark>}   % Font color for "Year", "#TRips" and "Dest." column labels
\def\TotalLabelFontColor{<mark>Blue</mark>}           % Font color "Total" column label
\def\PerTripLabelFontColor{<mark>Blue</mark>}         % Font color of column labels for "per trip" section
\def\YearTripsDestFontstyle#1{<mark>\textbf</mark>{#1}}% Bold-face "Year", "#Trips", "Dest." labels
\def\PerTripFontstyle#1{<mark>\textbf</mark>{#1}}     % Bold-face column labels for "per trip" section
\def\TotalFontstyle#1{<mark>\textbf</mark>{#1}}       % Bold-face column label "Total"
\def\YearFontstyle#1{<mark>\textbf</mark>{#1}}        % Bold-face "Yr1", "YR2", etc labels
</code></pre>
<b>The below table preamble gives you considerably MORE control over table layout than just changing parameter values.</b>
Copy/paste the below if you want to do things like remove or add vertical lines or change a column from left-alignment to center-aligned, for example. You can replace the \TaskWidth and other parameters with hard-coded numbers if desired, and change the "l" (left-align) to other alignment modes. You can change anything that is in highlight. Things that should NOT be changed (otherwise, the LaTeX will break) are the "T" variable and number of columns. 
<pre><code>
\newcolumntype{T}{
 <mark>|lcl</mark> >{\columncolor[\PerTripShadingColor]{\PerTripShadingTransparency}[\tabcolsep][\PerTripShadingMargin]}
 <mark>l</mark>>{\columncolor[\PerTripShadingColor]{\PerTripShadingTransparency}[\tabcolsep][\PerTripShadingMargin]}
 <mark>l</mark>>{\columncolor[\PerTripShadingColor]{\PerTripShadingTransparency}[\tabcolsep][\PerTripShadingMargin]}
 <mark>l</mark>>{\columncolor[\PerTripShadingColor]{\PerTripShadingTransparency}[\tabcolsep][\PerTripShadingMargin]}
 <mark>l</mark>>{\columncolor[\PerTripShadingColor]{\PerTripShadingTransparency}[\tabcolsep][\PerTripShadingMargin]}
 <mark>ll|</mark>
}   
</code></pre> 
</li>
<li><b>Examples</b>
The below is an example of how one can change the appearance of the table within a LaTeX document. After copy/pasting the code to incorporate the table into my document, I decided I wanted to turn the top blue header to green, and the gray shading to yellow shading (resulting in a hideous color scheme, by the way!). I copy/pasted the lines relevant to these formats. Here's what my LaTeX document looks like:  
<pre><code>
\include{do_NOT_manually_edit/isANONnonlabor}
% Put customizations for isANONnonlabor HERE
                                              
\def\BannerColor{Green}                   % Color of the top "Travel Cost Details" banner
\def\PerTripShadingColor{yellow}           % Shading color of "per trip" columns
\def\PerTripShadingTransparency{0.65}    % Shading transparency for "per trip" colunns; transparent(1.0) - opaque(0.0)

\begin{isANONnonlabor}
\caption{\normalsize \newline \newline
\textbf{Notes and assumptions}:
\newline \newline
While final destinations are not known at this time, domestic and international costs are estimated 
based on values taken from NASA Travel Guidebook using historical averages for a \daysPerDomesticTrip-- and \daysPerInternationalTrip--day 
conference for U.S. and European cities, resp., likely to host topical meetings aligned with the science of the proposed work. 
Domestic lodging and per diem rates are set by the GSA; international lodging and per diem are set by the Dept. of State (note 
that M\&IE is included in the per diem values shown here).
\newline \newline \noindent Yrs~1-2 funds will be used to present findings at science conferences and potentially to fund 
trips for collaboration with team members (i.e., NASA/GSFC).}
\newline \newline \underline{\scshape{domestic}}: 
per diem$+$M\&IE, car rental/day at \$\domesticPerDiemDollars and \$\internationalPerDiemDollars, resp.
\newline \newline \underline{\scshape{international}}: 
per diem$+$M\&IE, public transport/day estimated at \$\domesticGroundTravelDollars and \$\internationalGroundTravelDollars, resp.
\newline \newline \underline{\scshape{Travel Per Team Member}} 
(summed over \grantYears-year grant):
\newline
\perPersonNumberTripList
\newline All travel will be to present science results of this project at conferences and/or visits to home 
institutions of the team members for in-person collaboration. Note that above values above do not include 
institutional overhead.}
\label{tab:isANONnonlabor}

\end{isANONnonlabor}
</code></pre>
NOTE: To return to default values, all I have to do is comment-out (put a "%" at the line's beginning) the "\def" formatting lines that I pasted. 
</li>

<li><b>NUCLEAR OPTION:</b>
If you just cannot get the table to look like you want it to look, you can always copy/paste the entire table_isANONnonlabor.tex file that appears in the WorPT subfolder, into your document, and then edit at-will.  Some of the WorPT files involve complicated LaTeX code, so be sure that you have a good mastery of LaTeX and know what you are doing before implementing this option!
</li>
</ol>


