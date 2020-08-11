# Read 14a
<br>
<hr>
<br>

## Database Normalization
Database normalization is a process used to organize a database into tables and columns.  The main idea with this is that a table should be about a specific topic and only supporting topics included. 
* By limiting a table to one purpose you reduce the number of duplicate data contained within your database. This eliminates some issues stemming from database modifications.
* There are three main reasons to normalize a database.  The first is to minimize duplicate data, the second is to minimize or avoid data modification issues, and the third is to simplify queries. 
<br><br>

## Data Duplication and Modification Anomalies

Duplicated information presents two problems:

It increases storage and decrease performance.
It becomes more difficult to maintain data change

1. Insert Anomaly: There are facts we cannot record until we know information for the entire row.   Because in order to create the record, we need provide a primary key. 
2. Update Anomaly :In this case we have the same information in several rows. If we don’t update all rows, then inconsistencies appear.
3. Deletion Anomaly: Deletion of a row causes removal of more than one set of facts.  
