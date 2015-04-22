# How to get SQLite version

### Query

	select sqlite_version();

### File Check
* sqlite2 ==> first 48 bytes
* sqlite3 ==> first 16 bytes

#### Command
	$ head -c 48 file2.db
	** This file contains an SQLite 2.1 database **
	
	$ head -c 16 file3.db
	SQLite format 3

### Reference
<http://stackoverflow.com/questions/9646353/how-to-find-sqlite-database-file-version> 