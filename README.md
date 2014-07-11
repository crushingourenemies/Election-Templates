Election-Templates
==================

Templates for TNP Elections

In all the below templates, a word surrounded by double @ signs i.e. @@General@@ is to be substituted as appropriately defined:

1. Type: One of "General Election", "Judicial Election", or "Special @@Position@@ Election.
2. Position: One of "Delegate", "Vice Delegate", "Speaker", "Justice", or "Attorney General".
3. Month: the month during which the election begins.
4. Year: the year during which the election begins.
5. ShortLabel: For a scheduled election, the Month. For a special election, "Special Election".
6. NextSched: the month of the next scheduled election for the position(s) being elected.
7. EligibilityDate: the date one must have joined the Regional Assembly by to be eligible to run in the election (15 days before nominations are opened).
8. TermLimitedDelegate: a name or list of names of persons ineligible to run for Delegate due to term limitations.
9. CandidaciesOpen: the time candidacy declarations open as a UNIX timestamp (number of seconds since January 1st 1970, GMT). Determinable using [a tool](http://www.timestampgenerator.com/).
10. CandidaciesClose: the time candidacy declarations close as a UNIX timestamp.
11. VotingOpen: the time voting opens as a UNIX timestamp.
12. VotingClose: the time voting closes as a UNIX timestamp.
13. Eligible: the list of persons eligible to run for at least one of the positions.
14. NomCandidates: the list of valid candidates, each prefixed by [*] to itemize.
15. Nominees: the list of persons nominated who are eligible but have not accepted nomination, each prefixed by [*] to itemize.
16. DeclinedNominees: the list of persons nominated who are eligible but have declined the nomination.
17. InvalidNominees: the list of persons nominated who are ineligible to run.
18. Candidates: the list of candidates followed by "Abstain" or "Present" if Abstain is a candidate in this election, separated by " | ".
19. ChartURL: The URL of a pie chart image for election results, obtainable from an election counting spreadsheet..
20. CandidateVotes: the row in the results sheet's appropriate table for the candidate, prefixed by "[c]", for each candidate, concatenated.
21. ElectionCommissioners: the list of Election Commissioners, separated by ", ".

Any segment of a template which is enclosed in double square brackets i.e. [[[or not]] is understood to be excluded if unnecessary for the particular election.

## Template Candidacy Declarations topic OP

A Candidacy Declarations topic OP should include:

1. Instructions for candidates which cover:
    1. what positions are being elected;
    2. the eligibility requirements;
    3. how to make a nomination, accept one, or declare candidacy;
    4. when the deadline for acceptance of nominations and candidacy declarations is.
2. Optionally, a list of eligible members (Regional Assembly members who have been in the Regional Assembly since 15 days ago at the latest).
3. An easily readable listing of candidates and/or nominees.

Below is a template which covers these questions:

**Title**: Candidacy Declarations: @@Month@@ @@Year@@ @@Type@@ 

**Body**:

```
[center][big][b]Candidacy Declarations: @@Month@@ @@Year@@ @@Type@@[/b][/big]

[img]http://www.thenorthpacific.org/images/ec-seal.png[/img][/center]

This @@Label@@, The North Pacific will be electing [[a Delegate,]] [[a]] [[Vice Delegate,]] [[and]] [[Speaker,]] [[#]][[a]] [[Justice]][[s]][[,]] [[and]] [[an Attorney General]] to serve until the next election in [[NextSched]]. Any Regional Assembly member who has been a member for the last 15 days (since @@EligibilityDate@@) is eligible to run for these offices [[excepting that @@TermLimitedDelegate@@ is unable to run for Delegate due to term limitations]], and eligible members may run for more than one of these offices if they so wish. Loss of Regional Assembly membership before the conclusion of this election will also result in loss of eligibility to run for any office during this election. [[A list of those eligible to run is provided below.]]

To run, one must either accept a nomination or declare candidacy [u]in this thread[/u]. To withdraw from running, one must post a withdrawal of candidacy in [u]this thread[/u]. 

Acceptances of nominations, declarations of candidacy, and withdrawals of candidacy posted outside this thread will be discounted. Acceptance of a nomination is understood to also constitute declaration of candidacy even if no nomination has been made. Acceptances of nominations, declarations of candidacy, and withdrawals of candidacy must be posted during the candidacy declaration period to be valid. The candidacy declaration period is from (time=@@CandidaciesOpen@@) (your forum time) to (time=@@CandidaciesEnd@@) (your forum time). Voting will be approximately from (time=@@VotingOpen@@) (your forum time) to (time=@@VotingEnd@@) (your forum time).

This topic is intended for nominations, acceptances of nominations, declarations of candidacy, and withdrawals of candidacy; it may not be used for campaigning. Please keep in mind that lying about the election is election fraud, and that lying for any purpose is fraud.

[[[spoiler=Eligible to run*]@@Eligible@@[/spoiler]*Loss of Regional Assembly membership before the conclusion of this election will also result in loss of eligibility to run for any office during this election.]]

[b]Candidates:[/b][list=1]@@NomCandidates@@[/list]
[b]Nominees:[/b][list=1]@@Nominees@@[/list]
[b]Declined Nomination:[/b][list=1]@@DeclinedNominees@@[/list]
[b]Invalid Nominees:[/b][list=1]@@InvalidNominees@@[/list]

[i]Election Commissioners: @@ElectionCommissioners@@[/i]
```

The candidacy declarations topic should be pinned.
 
## Template Voting topic OP

A Voting topic OP should include:

1. Instructions for voters
    1. what positions are being elected
    2. who the candidates are
    3. how to vote (by post and/or by PM)
    4. when the deadline for voting is
2. a ballot template

Below is a template which covers these matters:

**Title**: Voting: @@Month@@ @@Year@@ @@Type@@ 

**Body**:

```
[center][big][b]Voting: @@Month@@ @@Year@@ @@Type@@[/b][/big]

[img]http://www.thenorthpacific.org/images/ec-seal.png[/img][/center]

Voting [[is now open]][[opens at (time=@@VotingOpen@@)]] in this @@Type@@ election. Voting will be from (time=@@VotingOpen@@) (your forum time) to (time=@@VotingEnd@@) (your forum time), and ballots submitted outside that time are invalid. 

Everyone who is a Regional Assembly member at the time voting opens is eligible to vote. Loss of Regional Assembly membership before the close of voting also results in loss of eligibility to vote.

Voters must use the following voting form:

[code][[[b]Delegate:[/b] < @@Candidates@@ >]]
[[[b]Would you like to reopen nominations?[/b] < Yes | No >]]

[[[b]Vice Delegate:[/b]: < @@Candidates@@ >]]
[[[b]Would you like to reopen nominations?[/b] < Yes | No >]]

[[[b]Speaker:[/b]: < @@Candidates@@ >]]
[[[b]Would you like to reopen nominations?[/b] < Yes | No >]]

[[[b]Court Justice (select 3) [[1]][/b]: < @@Candidates@@ >]]
[[[b]Would you like to reopen nominations?[/b] < Yes | No >]]

[[[b]Attorney General[/b]: < @@Candidates@@ >]][/code]

[[[b][color=red]Abstain is a candidate in this election. If you wish to abstain from voting you must use the option of PRESENT.[/color][/b]]]

Voters may submit their ballots either publicly by a post in this thread, or through personal message to [url=http://forum.thenorthpacific.org/msg/?c=2&mid=197430]The Voting Booth[/url]. Ballots not submitted according to these guidelines are invalid. Ambiguous votes are invalid.

[b][color=red]Election Commissioners are required by law to announce private votes in the voting thread, including the candidate(s) the vote was cast for, promptly after those votes are cast. For this reason, voters are discouraged from announcing, as was custom, that they have voted privately, as the subsequent public declaration by the Election Commissioners can potentially reveal how they voted.[/color][/b]

Please do not post anything other than your ballot in this thread. If you have any questions please send them directly to [url=http://forum.thenorthpacific.org/msg/?c=2&mid=197430]The Voting Booth[/url] or start a new thread. Additional and unnecessary comments will be removed.

[i]Election Commissioners: @@ElectionCommissioners@@[/i]
```

The voting topic should be pinned.

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

A Results post must cover:

1. That the votes have been counted
2. How many votes were counted for each candidate, and how many abstained
3. Which publicly posted votes were invalid, if any (this can be addressed by inserting a note using the BBCode [note] tag following the affected total, or by adding a separate paragraph).
4. Who, if anyone, is elected to which position
5. Whether a runoff will be held

Below is a template which covers these questions:

**Title**: Results: @@Month@@ @@Year@@ @@Type@@
**Body**:

```
[center][big][b]Results: @@Month@@ @@Year@@ @@Type@@[/b][/big]

[img]http://www.thenorthpacific.org/images/ec-seal.png[/img][/center]

The Election Commission has counted the votes in this @@Month@@ @@Year@@ @@Type@@ and now publishes these results, attesting they are true and correct.

[[[center][img]@@ChartURL@@[/img][/center]]]

[[[table=4,Delegate, 1]Candidates[c]Votes[c]Elected[/table]]]
[[[table=4,Vice Delegate, 1]Candidates[c]Votes[c]Elected[/table]]]
[[[table=4,Speaker, 1]Candidates[c]Votes[c]Elected[/table]]]
[[[table=4,Court Justice, 1]Candidates[c]Votes[c]Elected[/table]]]
[[[table=4,Attorney General, 1]Candidates[c]Votes[c]Elected[/table]]]

[[A detailed breakdown of votes and results can be found in [url=@@SpreadsheetLink@@]this spreadsheet[/url].]]

[i]Election Commissioners: @@ElectionCommissioners@@[/i]
```

The results topic should be pinned.

## Template unread-PM

You probably received a link to this manual from a PM which was sent to The Voting Booth by the previous election commission and left unread and unfiled. Please send a PM of the same kind to the next Election Commission:

**Title**: A Note to our Successors

**Body**:
```
To whomever next takes this solemn duty,

It has been our experience that the operation of elections in The North Pacific requires great care to avoid being unfair in one direction or another and ensure democracy functions. To assist future Election Commissions in taking such appropriate care, we pass on a set of [url=https://github.com/The-North-Pacific/Election-Templates]Templates[/url] and instructions. We recommend that as your first act, you adopt the protocol that actions following these instructions may be taken by any Election Commissioner individually (to save time) but any deviation from them should be voted on (to reduce the risk of error).

The very best of luck,
You just might need it,
~The Previous Election Commission
```

If any part of this manual did not meet the needs of you or your Election Commission as a whole, please suggest improvements. The canonical way to do so is via a [pull request](https://help.github.com/articles/using-pull-requests) but if that's not your piece of cake, just PM one of the people who _would_ do that. Any change requested by an Election Commission will be made.
