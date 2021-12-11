# unsupported-sql-extracter for  https://github.com/apache/shardingsphere/issues/13792

1. Get All SQL files: We have SQL files at the following location
https://github.com/postgres/postgres/tree/master/src/test/regress/sql

2. Run SQLParserEngine: For each SQL files run SQLParserEngine and extract SQL which causes an exception
For running SQLParserEngine I can refer to https://github.com/tuichenchuxin/extract-sql-for-shardingsphere-parser-test

3.Add to Unsupported: Find SQL which is causing the exception. Add it to unsupported.xml
https://github.com/apache/shardingsphere/blob/master/shardingsphere-test/shardingsphere-parser-test/src/main/resources/sql/unsupported/unsupported.xml

4. Confirmation Step: Run UnsupportedSQLParserParameterizedTest.java test.
Test should pass and SQLParsingException should be thrown for the SQL which was added in step 3.

