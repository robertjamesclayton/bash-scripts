# bash-scripts

# tcm

**usage: tcm [[-s YYYY-MM-DD] [-u YYYY-MM-DD]] | [-t]**

Display number of lines added and deleted and total commits over a date range for all committers to the current working directory git repo. Use with no arguments to get stats from the first day of the current month.

*-t print details of the number of unit tests added by usernames instead of lines added deleted (may take a while to run)*

*-s optional start date YYYY-MM-DD*

*-u optional end date YYYY-MM-DD*

**Examples**

tcm -s 2017-05-01 -u 2017-08-31

COMMITTER            ADDED      DELETED    COMMITS    
rwilson&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;75&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;47&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;8          
rhansen&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;282&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;97&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;9          
epeters&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;316&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;87&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;7          
gsinger&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;61&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;23&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1     

tcm -t

COMMITTER&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;NO. UNIT TESTS    
rwilson&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;75<br/>
phansen&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;43<br/>
ataylor&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;43<br/>

*download tcm script to /usr/local/bin then 'chmod +ux /usr/local/bin/tcm'*

# ccrev

**usage: ccrev -t title -r reviewer -o observer -c**

Adds and starts a Code Collab review using the last git commit (HEAD^) as the source of git diff. The reviewer and observer must be valid Code Collab user names.

#### Installation

Install node, easiest way is via installer https://nodejs.org/en/download/ . You will also need the jira command line utilities: npm install -g jira-cmd

**Example**

ccrev -t "Added unit tests to new fancy service" -r pwilson -o tdavis
