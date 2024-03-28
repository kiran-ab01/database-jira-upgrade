# database-jira-upgrade
8.20(PostgreSQL 10) to 9.4.12(PostgreSQL 12)

first upgrade postgress to 12 then jira


while upgrading db we need to check jira postgres version compatible with jira versions

db upgrade 

from 10 to 12 postgress

if we upgrade old db will loss

so need to take backup


create new db and user after upgrade

need to restore the db

psql databasename < dabase.sq(pg_dum jiradb > database.sql)

after we need to change dbconf.xml -->to new db


stop postgress-12(newqly updated version)

pg_hba.conf

we need to trust

postgress.conf

-->uncomment the local host

--> start postgres-12

--> start jira


--> validate

-->check all the lince of plugin before unable

--> validate the suported version for plugin jira

-->don't desable universal plugin(system), atalsian truble shoot

stop jira


to upgrade jira from 8.20 to 9.4


--> downlod binary files jira


before  major upgrade we need to check some changes like

--> check the atlassian doc

(https://confluence.atlassian.com/jirakb/how-to-upgrade-jira-8-to-jira-9-with-minimal-downtime-1115137250.html)

fix db.conf --> pool size to 40

fix jira-config.properties --> set atoumatica reindex = false








