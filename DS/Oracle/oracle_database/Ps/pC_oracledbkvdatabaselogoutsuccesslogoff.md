#### Parser Content
```Java
{
Name = oracle-db-kv-database-logout-success-logoff
  Vendor = Oracle
  Product = Oracle Database
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSSSS"
  Conditions = [ """.sql.AUDIT_TYPE="Standard Audit"""", """.sql.STATEMENT_TYPE=LOGOFF""", """.sql.DB_USER=""", """.sql.USERHOST=""" ]
  Fields = [
    """sql\.EXTENDED_TIMESTAMP="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d.\d{6})"""",
    """sql\.USERHOST=({host}[^=]+?)\s*("|,|$)"""
    """sql\.OS_USER=({user}[\w\.\-]{1,40}\$?)\s+[\w\.]+?=""",
    """sql\.DB_USER=({account}[^=]+?)\s+[\w\.]+?=""",
  ]


}
```