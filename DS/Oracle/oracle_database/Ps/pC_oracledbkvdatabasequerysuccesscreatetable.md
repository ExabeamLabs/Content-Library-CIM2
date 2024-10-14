#### Parser Content
```Java
{
Name = oracle-db-kv-database-query-success-createtable
   ParserVersion = "v1.0.0"
   Conditions = [ """.sql.AUDIT_TYPE="Standard Audit"""", """.sql.STATEMENT_TYPE="CREATE TABLE""", """.sql.DB_USER=""", """.sql.USERHOST=""" ]
   Fields = ${OracleParsersTemplates.oracle-db-template-2.Fields}[
     """sql\.STATEMENT_TYPE="({db_operation}[^=]+?) TABLE"\s+[\w\.]+?="""
   ]
 
oracle-db-template-2 = {
  Vendor = Oracle
  Product = Oracle Database
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSSSS"
  Fields = [
    """sql\.EXTENDED_TIMESTAMP="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d.\d{6})"""",
    """sql\.USERHOST=({host}[^=]+?)\s*("|,|$)"""
    """sql\.OBJECT_NAME=({db_object}[^=]+?)\s+[\w\.]+?=""",
    """sql\.OBJECT_SCHEMA=({db_schema}[^=]+?)\s+[\w\.]+?=""",
    """sql\.USER=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+[\w\.]+?=""",
    """sql\.DBID=({db_name}[^=]+?)\s+[\w\.]+?=""",
    """sql\.DB_USER=({account}[^=]+?)\s+[\w\.]+?=""",
    """sql\.SQL_TEXT="({db_query}[^@]+?)\s*"\s+[\w\.]+?=""",
    """sql\.RETURNCODE=({return_code}[^=]+?)\s+[\w\.]+?=""",
    """sql\.OS_USER=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+[\w\.]+?="""
  ]
  DupFields = [ "account->db_user" 
}
```