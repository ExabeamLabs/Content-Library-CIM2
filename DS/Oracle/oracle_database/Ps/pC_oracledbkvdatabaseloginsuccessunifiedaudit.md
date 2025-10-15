#### Parser Content
```Java
{
Name = oracle-db-kv-database-login-success-unifiedaudit
   Vendor = Oracle
   Product = Oracle Database
   ParserVersion = "v1.0.0"
   TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
   Conditions = [ """ACTION:"100"""", """DBUSER:"""", """DBID:"""", """Oracle Unified Audit"""]
   Fields = [
     """({host}[\w\-.]+)\s+(?:journal:)?\s+Oracle Unified Audit""",
     """DBID:\s*"+({db_id}({db_name}\d+))""",
     """DBUSER:\s*"+({db_user}[^":]+)""",
     """CURUSER:\s*"+({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
     """ACTION:"({db_operation}100)"""",
     """RETCODE:"({return_code}\d+)""""
    ]
 

}
```