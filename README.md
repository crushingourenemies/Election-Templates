Election-Templates
==================

Templates for TNP Elections

## Template Nominations topic OP

A Nominations topic OP should include:

1. Instructions for candidates which cover:
    1. what positions are being elected
    2. the eligibility requirements
    3. how to file a nomination, accept one, or declare candidacy
    4. when the deadline for nominations / declarations is
2. Optionally, a list of eligible members (Regional Assembly members who have been in the Regional Assembly since 15 days ago at the latest)
3. An easily readable listing of nominees and/or candidates

ACTUAL TEMPLATE GOES HERE OR ALTERNATIVELY IN SEPARATE FILE

## Template Voting topic OP

A Voting topic OP should include:

1. Instructions for voters
    1. what positions are being elected
    2. who the candidates are
    3. how to vote (by post and/or by PM)
    4. when the deadline for voting is
2. a ballot template

ACTUAL TEMPLATE GOES HERE OR ALTERNATIVELY IN SEPARATE FILE

## Counting spreadsheet template

A publicly visible Elections template is provided [here](https://docs.google.com/spreadsheet/ccc?key=0AqCj7Gv_2W_MdEhuNzctQ0xqWXhwdmNaN0QxQXNMYkE#gid=0)

### Instructions for cloning

1. You can copy the counting template by opening it, clicking the File menu in the upper left hand corner, and clicking "Make a copy..."
2. It is generally advisable to share the counting sheet with all Election Commissioners.
3. To update the copy of the template for the current election:
    1. Remove the charts in the Results sheet for all positions which are not being elected (click on the chart, then click on the drop down menu in the upper right hand corner of the chart and select "Delete chart")
    2. Remove the columns in the Results sheet for all positions which are not being elected (select the columns by clicking on the column label of the first and dragging across to the last, then click the drop down menu at the right end of the column labels and select "Delete columns *Letter* - *Letter*"
    3. Update the date voting begins in cell Voters!G3
    4. (optional) Update the conditional formatting of the "Date Joined" column
    5. Update the set of candidates in the Results sheet.
    6. If more candidates are needed than there are spaces, the macros under the **Percentage** and **Win?** columns will need to be updated by extending the range they apply to. The range deliberately excludes the row for abstentions.
4. After setting things up, it is advisable (though not required) to set the verification scripts which check the list of TNP nations and the dates members joined the RA to run automatically. To do this:
    1. Enter the script editor by clicking the Tools menu at the top and selecting "Script editor..."
    2. Open the Triggers dialog by clicking the Resources menu at the top of the script editor and selecting "Current project's triggers"
    3. Click the link to add a trigger in the Triggers dialog.
    4. The default trigger should specify the verify\_all function, on a event "From Spreadsheet" which is "On open". If it does not, update the fields to call the verify\_all function whenever the document is opened, as above.
    5. Save the trigger by clicking the Save button.

### Instructions for counting

1. For every public vote, one can enter the voter's forum name, their TNP nation, and their votes (as well as any notes if needed) in the Public Ballots sheet in the appropriate columns.
2. For every private vote, one can do the same in the Private Ballots sheet. (The Private Ballots sheet must _never_ be published).
3. Check the Voters sheet for invalid votes.
4. Invalid votes can be invalidated by adding a prefix or suffix to the vote, e.g. "- Candidate's name" instead of "Candidate's name".
5. It is advisable to inform invalid voters that their vote is invalid in shortly after they cast it, allowing them to correct any errors if possible.

## Important Note regarding Private Votes

Because we allow private votes, the entire spreadsheet cannot be published. One can publish anything except the Private Ballots sheet, though it is traditional not to publish the full list of private voters so the Voters sheet should not be published lightly.

After the election is concluded, it is generally advisable to put all private ballot PMs into a folder, to afford future Election Commissions a clean working environment.

## Template Results topic OP

TEMPLATE GOES HERE

TEMPLATE SHOULD COVER:

1. optional inclusion of charts from spreadsheet template
2. vote count table template

## Template unread-PM

You probably received a link to this manual from a PM which was sent to The Voting Booth by the previous election commission and left unread and unfiled.
