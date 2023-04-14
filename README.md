# WorPT: <b>Wor</b>P**lan-**T**ool (for proposals)
This script is attached to a Google Sheet and allows one to generate Latex tables that may be included in a Latex document written for a research grant proposal using a form of the "\input" command (detailed instructions appear in the Latex files that are generated as comments at the top of the files).  The tables describe the proposal's work-plan and associated schedules and labor distribution among the proposing team, and are rendered in 2 different versions:  an anonymous and non-anonymous version for inclusion in dual-anonymous-reviewed grant programs.  The tool allows one to make tweaks, additions, deletions and quickly re-render the new versions of these tables without worrying about human error or inconsistencies that arise when such edits are performed manually.

The below is a link to the Proposal Work Plan Tool spreadsheet on Google Drive:
https://docs.google.com/spreadsheets/d/1HJgQHlg86lJtBBuUYYUnHpsc07QheXRoozOXpvx1uTg/copy

and here is a link to the bio-sketch template that is also used in the script: 
https://docs.google.com/spreadsheets/d/1h_6lBru9ZOgCkqyNvUSHPj_42HnXFPNCbhsRbu5HEW8/copy

If you hit the "Copy" button that appears when you follow the above links, copies of the spreadsheets will appear on the "Shared With Me" folder in your Google Drive. Those copies, which will include the attached script that makes Proposal Work Plan Tool work, are yours to use as you write your own grant proposals. You should move the Proposal Work Plan spreadsheet down into a designated folder for the proposal you are working on, which is where the latex files that are generated by the script will also be placed. 

The bio-sketch template should be moved into a folder that will hold the bio sketches of all the colaborators you work with on proposals.  This folder will serve as a sort of one-stop-shop for your collaborators to edit their bio sketches to keep them current over time, so that they don't have to create a whole new bio sketch every time you write a new proposal. 

To be explicit, let's say you created a Google Drive folder called "proposal2022" under another folder that holds all your proposal materials.  The folder/file structure that you start out with should look something like: 

          /AllProposals/ProposalsIn2022/ADAP2022/Proposal Work Plan verxxxxxxx

And then you might want to keep all the biosketches just under AllProposals, so you make a subfolder called bioSketches and then place the google sheet template under that folder:

          /AllProposals/bioSketches/biosketch

Copes of the biosketch google sheet template should be made, one for each collaborator you anticipate working with on the proposal. Something like:

          /AllProposals/bioSketches/BobSmith-biosketch
          /AllProposals/bioSketches/SallyJackson-biosketch
          /AllProposals/bioSketches/JanePerry-biosketch
          
The biosketch folder is one that can be added to over time, and each biosketch can be edited and maintained over time to keep the information up-to-date. 

The script should be ready to start accepting input, right out of the box. You may have to "accept permissions" when you try running "LIBRARY FUNCTIONS -> UPDATE LIBRARY" the first time.

Feel free to contact me if you run into permission problems or if you notice any bugs as you use the code.

*****NOTE: the below method works but is outdated -- a much easier process is now in place that works with GitHub -- I will make a new video soon, that shows how to use a one-button push to inject ALL the files generated by Proposal Work Plan Tool into your Overleaf project!*****
A video that describes Proposal Work Plan Tool and walks through all of its functions, including how to link the generated Latex table files on Google Drive with your Overleaf project, is provided at this YouTube link: https://youtu.be/a3tGQopb0QI

     %%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
     %%%%%%%%%%  Thank you for your interest in Proposal Work Plan Tool !  %%%%%%%%%
     %%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

Updates: ver 04142023 is the latest version
--------------------------------------------------------------
04/14/2023
  minor tweaks with biosketch template:  the "PUBLICATIONS" sheet now self-populates the Overleaf ID numbers along the top right side, copying from the Overleaf IDs provided by the user on the BACKGROUND sheet.  Also, a script is now attached to the biosketch files which runs when the user edits the Overleaf ID area in the BACKGROUND sheet and adds more columns to the Overleaf ID area in the PUBLICATIONS sheet, if fewer columns are present than for the BACKGROUND Overleaf ID section. 
--------------------------------------------------------------
03/29/2023
  bug-fix: Due to an indexing error, the first 6 publications at the top of the list in the bio-sketch file were ignored. A further complication of this indexing error was that the checked boxes indicating which publications to use for a proposal were correspondingly mis-aligned with the intended publications.  This indexing error is now resolved and all publications that are indicated by a checked box should now appear in the rendered bio-sketch. 
  IMPACT:  although such was not necessary to fix the indexing error, a measure was taken to make the PUBLICATIONS sheet of the bio-sketch file more robust, by defining a new "named range".  Therefore, the previous biosketch files will now be incompatible with the 03292023+ versions of Work Plan Tool.  
  
  IF YOU DO NOT WANT TO COPY OVER ALL YOUR INFO INTO THE NEW BIO SKECTH FILE TEMPLATE, then you can retrofit your existing bio sketch files by doing the following for each file:  
          (1) open up the bio sketch file (you will need to apply these steps to each of the bio sketch files that you have)
          (2) click on the PUBLICATIONS tab at the bottom to bring up the PUBLICATIONS sheet. 
          (3) right-click to select the entire row on which the column heading "CITATION" and "ADD TO OVERLEAF PROJECT?" are located.  Make sure the entire row is selected (in the template, this row would be row #6 in the spreadsheet), then choose "View More Row Actions", then "Define Named Range". 
          (4) in the textbox that comes up in the sidepanel, replace the default "NamedRange1" with "_pHeaderRow" (but without the quotes).  Make sure that you replicate the lower and upper case letters precisely, and don't forget the underscore at the beginning.   The text box underneath should have automatically populated to say "PUBLICATIONS!6:6", if row #6 is indeed where the "CITATION" and "ADD TO OVERLEAD PROJECT?" appear.  
          (5) Hit "Done" button, then close the side panel by clicking on the upper right corner "X"
Your bio-sketch files should now be compliant with the latest Work Plan Tool.  Or skip the above and just copy over all the info from your existing bio-sketch file(s) into the new templates. 
--------------------------------------------------------------
03/28/2023
  Significant changes have been made to add new functionality. 
  - 2 new Latex files are now generated (for a total of 11 .tex files that generate tables):
        * a table that generates the travel budget (using information entered by the user in a new travel area in the Work Plan Tool.
        * a table that generates the "non-labor" budget (Equipment, a rolled-up travel budget summary, publication fees, etc.) 
  - Related to these 2 new Latex table files: 
        * A new "TRAVEL" section in the right side of the "PERSONNEL & FTE" sheet, where the anticipated NUMBER of annual trips for both domestic and international travel may be entered for each funded team member.  The number of trips is used to later generate a travel budget table. 
        * Created a new sheet for editing: "NONLABOR BUDGET", where the user enters ItTEMS such as "Equipment", "Materials & Supplies", etc along with a yearly budget amount. This information gets turned into one of the new Latex table files.  Also on this sheet are parameters to input related to travel, for both domestic and international trips:  airfare, per-diem, conference fees, ground transportation, and the typical number of days for a trip.  Also included is the option to allow for annual percent-increases (cost-of-living adjustments) that can be entered as different rates for these different categories (or set to zero for a flat budget profile).  

Also, changes unrelated to the 2 new tables include: 
  - "HELP" buttons are now on each sheet.  When the user clicks the button, a sidepanel will appear, providing additional inforamtion regarding the usage of the sheet that the user is actively looking at. 
  - A new column in the "PERSONNEL & FTE" sheet, "FTE accuracy", allowing the user to specify the accuracy to perform rounding of summed FTEs displayed in the right FTE columns of that sheet.  For example, an accuracy of "0.01" would cause a summed FTE value of 5.3226 to turn into 5.33, while an accuracy of "0.05" would turn the value into 5.35  (rounding up to nearest interval of 0.01 and 0.05, resp.)
  - The "Add New Team Member" button is gone from the PERSONNEL & FTE sheet, and the "Add a new TOP TASK row" and "Add a new SUB LEVEL TASK row" buttons are gone from the TASKS sheet.  All new rows for both sheets are added in a more natural way using the conventional Google Sheet method for adding rows (right-click where you want the new row, then select add row).  The previous buttons were clunky and time-consuming because a script ran when the buttons were selected, so I am quite happy to see them gone!  The buttons were originally needed to insure that new rows were populated with the appropriate formulas and formatting, and could be done away with by sneakily embedding all formulas into the column headings as array formula, so that they are less likely to be accidentally edited, will apply uniformly to all new rows without having to invoke a script, and  just provide a cleaner interface. This new formatting of formulas was only possible by Google's recent introduction of "Named Formulas", which Work Plan Tool now makes extensive use of. The result is a cleaner, faster and more easy to maintain spreadsheet (Thank you, Google!) 
  - A checkbox to toggle the option of including the proposal in the "Current/Pending" funding status pages.
  
A new copy of the BioSketch template is also made available, with just minor changes from the previous version (some column headings were re-worded for clarity).  Your old biosketches should be compatible with the latest version of the Work Plan. 

*I plan to create a new YouTube video walking through the new Work Plan Tool, as the tool is now so different from the version that the last video was based on, that a new video is warranted.  That YouTube link will be posted here, when ready for publication.*
---------------------------------------------------------------
08/17/2022
  Major changes have been made to add new functionality. 
  - 2 new Latex files are generated:  
        * a table specific for inclusion in an HST Phase II proposal that gives team member, institutional affiliation (and whether US or foreign), role on proposed project, level of effort (FTE) on the project.
        * a table that approximately replicates the spreadsheet presentation in the "TASKS" tab of the Work Plan tool, with task and sub-task titles, the timeline, the task lead and expert assignments to each sub-task, and the total FTEs involved on each task. 
  - New columns have been added to the "PERSONNEL & FTE" tab/sheet: 
        * Institutional Affiliation (Name, Position, US or Foreign)
        * Checkbox to indicate the persons whose bio sketch should be included in the proposal
        * Checkbox to indicate the persons whose funding status should be included in the proposal
        * Checkbox to indicate if bio sketches should be included on separate pages or not.
        * Checkbox to indicate if current/pending funding status should be included on separate pages or not.
  - A new tab/sheet called "GENERAL INFO" was created, to help clean up the busy appearance on the "PERONNEL & FTE" sheet.  On the GENERAL INFO sheet, the name of the funding program, overleaf project ID number, Overleaf project title and Full proposal title fields are present. 
  - The "TASKS" sheet has been modified such that if a collaborator is entered with the number of weeks, the number of weeks is immediately copied over into the "not funded by this grant" column. (This functionality required the addition of a "onEdit" function to be added to the script, which runs every time the spreadsheet is edited, and therefore might cause a bit of a delay relative to its speed before this modification.) 

Changes were also made to the Bio Sketch file: 
  - A new column "Admin PI" was added to the "GRANT SUPPORT" page. 
  - A new column "date" was added to the PUBLICATIONS page (Note that this column is not used by the script -- it is there only to conduct sorting on that page to help make the page easier to view by having the publications ordered in a timeline)
  - Column labels were changed on the BACKGROUND page:  instead of "years", the word "timeline" appears in order to make the intended contents more clear. 
  - On all the tabs/sheets, a note about the need to write in Latex-friendly text was given, as well as mention of the fact that the script will sort items in the proper timeline, so the user should not try to copy/paste new rows to forcefully do that ordering themselves (The concern is that some copy/paste might remove needed equations or formating from the cells). 
---------------------------------------------------------------
05/19/2022
  - Following using the scripts to get a proposal submitted this week, I've made more tweaks and one substantial change:  All files generated by Proposal Work Plan Tool now are also copied into a GitHub repository, where they can then be linked to your Overleaf project using a single button-push.  I will post instructions and video as soon as possible that demonstrate this wonderfully convenient new capability! 
--------------------------------------------------------------
05/09/2022
  - I've made several small tweaks to the code and have forgotten what most of the tweaks were.  But the MAJOR change was incoporating bio sketches.  Now, each collaborator can fill out the biosketch template (a google sheet) and maintain it over time.  The script sweeps up all the bio sketch information and then formats each bio sketch into a uniform template. The advantage of this approach is that one can list ALL of their publications, etc. but use the righthand columns in the sheet to indicate whether that publication should be listed in the bio sketch for that proposal or not.  Some publications might be relevant only to certain proposals, but the spreadsheet allows one to store all that information in one place. 
--------------------------------------------------------------
12/10/2021
  - corrected an error in the script that kept some of the tables from rendering correctly because of an indexing issue that caused the code to grab the wrong columns of FTE data. 
  - corrected the script so that it now properly removes any columns of years in the FTE tables for which the proposal has no FTEs assigned.  For example, if the proposal is only a 2-year grant, then only 2 years will be shown in the LAtex tables and will not waste space showing years 3, 4 and 5 that have only 0 FTEs in them.
  - corrected a few minor bugs (like the FTE sub-totals in the upper right cover of the TASKS tab not showing correct in-kind contributions).
  - added ability to select "student" collaborator designations ("st(1)", "st(2)", etc.)
  - changed the cell in the  ANONtasks tab (a hidden tab) that controls the table footnote to be a more generic text, and flagged the cell so that it can be easily found by the user and the text changed to whatever is desired (a note is now appended to that cell to describe how to change the text). 
  - flagged the cells in several other latex template files (e.g., NOTANONtasks, NOTANONpersonnel_work_effort, etc tabs) to indicate where one might change the color schemes of the Latex tables, if desired -- see the notes that are attached to the flagged cells for details). 
