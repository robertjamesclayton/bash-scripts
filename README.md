# bash-scripts

# tcm

**usage: tcm [-s YYYY-MM-DD] [-u YYYY-MM-DD]**

Display number of lines add and deleted and total commits over a date range for all committers to the current git repo.
 with no arguments to get stats from the beginning of the current month.

**Example**

tcm -s 2017-05-01 -u 2017-08-31

COMMITTER            ADDED      DELETED    COMMITS    
rwilson              75         47         8          
rhansen              282        97         9          
epeters              316        87         7          
gsinger              61         23         1          

*download to /usr/local/bin*
*chmod +ux
