<b>WorPT Packages</b> need to be installed in your LaTeX document's preamble in order to use a WorPT file in your LaTeX document.  
<hr>

<mark><b>How To Install WorPT Package Files In Your Document</b></mark>
<p>
You only need to install the WorPT Package files <b>ONCE</b>. After you have installed the WorPT Package files, you can incorporate as many of the WorPT files as you want, into your LaTeX document. 
</p>

<p>Choose one of the 2 below options, depending on if you are using the AAS document class file (which already incorporates some of the packages bundled in the WorPT Package files) or a non-AAS class file. </p>

<details>
<summary><b>if using aastex.cls</b></summary>
COPY contents of the following 3 files into your own 3 files.
<ol>
 <li>https://github.com/pmarcum/LaTex-Formatting/blob/main/aas-style/FUformatting.sty</li>
 <li>https://github.com/pmarcum/LaTex-Formatting/blob/main/aas-style/FUpackages.sty</li>
</ol>
You might also find the following helpful, although it is not necessary for the WorPT tables:
<ol>
 <li>https://github.com/pmarcum/LaTex-Formatting/blob/main/aas-style/FUnewCommands.sty</li>
</ol>
</details>

<details>
<summary><b>if using a different document class file</b></summary>
COPY contents of the following 3 files into your own 3 files. 
<ol>
 <li>https://github.com/pmarcum/LaTex-Formatting/blob/main/general/FUformatting.sty</li>
 <li>https://github.com/pmarcum/LaTex-Formatting/blob/main/general/FUpackages.sty</li>
</ol>
You might also find the following helpful, although it is not necessary for the WorPT tables:
<ol>
 <li>https://github.com/pmarcum/LaTex-Formatting/blob/main/general/FUnewCommands.sty</li>
</ol>
</details>

Incorporate the files you just copied, into your LaTeX document, by putting the following into your LaTeX document's preamble.<br>
These lines should be inserted somewhere <b>between the \documentclass[]{} and \begin{document} lines</b> in your document. <i>Assumes you named the copied files the same filenames as the original github ones.</i><br>
Highlights indicate where edits might be needed.
<pre><code>
\usepackage{<mark>FUpackages</mark>}  % applying Frequently-Used packages
\usepackage{<mark>FUformatting</mark>} % apply Frequently-used formatting definitions/setups
\usepackage{<mark>FUnewCommands</mark>} % <b>[OPTIONAL]</b> apply Frequently-used usercommands  
</code></pre>

<p>If you have conflicts between the packages in the WorPT Package files and your LaTeX class file, then comment out the conflicting lines in the local copies of the WorPT Package file(s) and determine if the WorPT tables will compile correctly with those lines commented out.</p>
