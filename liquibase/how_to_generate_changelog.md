# What is liquibase 
- reference site : https://docs.liquibase.com/home.html#
- liquibase is db migration tool like the flywaydb

# How to install
https://docs.liquibase.com/install/home.html


# Command Line
- guide : https://docs.liquibase.com/commands/generatechangelog.html?Highlight=generateChangelog

## DDL Export
---

liquibase  
--driver="{driver_type}"
--classpath="{driver_location}" 
--changeLogFile="{output_file}"
--url="jdbc:postgresql://{url}:{port}/{database_name}" 
--username="{connection_user_name}" 
--password="{connection_password}" 
--diffTypes="{target_scope}" 
generateChangeLog

--- 

### example
liquibase --driver=org.postgresql.Driver --classpath="{driver location}" --changeLogFile=dml_changelog.xml --url="jdbc:postgresql://{url}:{port}/{database_name}" --username=test --password="1234" --diffTypes="tables,views,columns,indexes,foreignkeys,primarykeys,uniqueconstratints" generateChangeLog
 
## DML Export
---

liquibase  
--driver="{driver_type}"
--classpath="{driver_location}" 
--changeLogFile="{output_file}"
--url="jdbc:postgresql://{url}:{port}/{database_name}" 
--username="{connection_user_name}" 
--password="{connection_password}" 
--diffTypes="data" 
generateChangeLog 

---