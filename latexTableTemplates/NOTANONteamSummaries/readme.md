<b>NOTANONteamSummaries</b> is a file containing a paragraph for each team member describing the role in the proposed project. The file is generated from the text written in the WorPT spreadsheet under "ROLE/BACKGROUND NARRATIVE" on the PERSONNEL & FTE page. The person's name is attached to the beginning of the paragraph and boldfaced. 

<font size="3">WorPT table example: <b>NOTANONteamSummaries</b></font>
<br>
<img src="https://lh3.googleusercontent.com/d/1ElfTFpZPTL4-SBHa9G2IzOQ0GBVEouUf" width=30%>
<hr>
<b>HOW TO USE:</b>
<ol>
<li><b>Special WorPT Packages</b> [<i>one-time-only task</i>] Copy/paste the special packages in preamble of your document, if you haven't done so previously. (see https://github.com/pmarcum/WorPT-Work-Plan-Tool-4-proposals/blob/main/WorPTpackages for more info).</li>
<li><mark><b>How To Put File Contents Into Your Document</b></mark> [<i>do once for inclusion of this file</i>] 
<ol>
<li>COPY the lines in the code block below, then</li>
<li>PASTE into your document WHERE you want the content to appear, then</li>
<li>MODIFY the editable lines you just pasted in your document as needed. The lines that may be edited (or even deleted altogether if not wanted) are indicated by highlight below. </li>
</ol>
   
<pre><code>
\newpage       % You can comment out or use \clearpage instead
\include{do_NOT_manually_edit/table_NOTANONteamSummaries}  % replace do_NOT_manually_edit with correct folder name if something different
<mark>% Put customizations for NOTANONteamSummaries HERE</mark>
\begin{NOTANONteamSummaries}
\end{NOTANONteamSummaries}  
</code></pre>
</li>

<li><b>Customize appearance</b> [<i>do as many times as needed</i>]
The default settings produce a nice-looking file, so you probably won't have to do any customization for this file. The options for changing the appearance are severely limited for this file.
<ol>
<li>COPY any or all lines in the code block below that are related to the formatting parameter that you want to edit. The lines below show default values. You will edit those values to make desired changes.</li>
<li>PASTE the copied lines into your document at the "% Put customizations for NOTANONteamSummaries HERE" line in the code that you copy/pasted in Step 2. Most importantly, the desired formatting lines should be pasted somewhere <b>between</b> the \include{do_NOT_manually_edit/table_NOTANONteamSummaries} and \begin{NOTANONteamSummaries} lines. </li>
<li>EDIT the pasted lines in your document, as desired. Some examples are given at the bottom of this page.</li>
NOTE: you can PICK AND CHOOSE the lines you want to paste into your document; you do not have to copy/paste all of the below lines!
</ol>
<b>The below line is the only option for changing the format. Highlights indicate what can be edited:</b>    
<pre><code>
\def\NameBoldface#1{<mark>\textbf</mark>{#1}}             % boldface the name at top of paragraph for that person
</code></pre>
</li>

<li><b>Examples</b>
The below is an example of how one can change the appearance of the contents within a LaTeX document. I copy/pasted the only formatting line that controls font style and edited so that the name is both boldfaced and italicized. Here is a peek at what my LaTeX document looks like:  
<pre><code>
\newpage       % You can comment out or use \clearpage instead
\include{do_NOT_manually_edit/NOTANONteamSummaries}  % replace do_NOT_manually_edit with correct folder name if something different
% Put customizations for NOTANONteamSummaries HERE
  
\def\NameBoldface#1{\textbf{\emph{#1}}}              % boldface name/role

\begin{NOTANONteamSummaries}
\end{NOTANONteamSummaries}
</code></pre>
NOTE: To return to default values, all I have to do is comment-out (put a "%" at the line's beginning) the "\def" formatting lines that I pasted. 
</li>

<li><b>NUCLEAR OPTION:</b>
If you just cannot get the content to look like you want it to look, you can always copy/paste the entire table_NOTANONteamSummaries file that appears in the WorPT subfolder, into your document, and then edit at-will.  Some of the WorPT files involve complicated LaTeX code, so be sure that you have a good mastery of LaTeX and know what you are doing before implementing this option! (But this particular file is extremely simple!)
</li>
</ol>
