#### Parser Content
```Java
{
Name = oracle-db-kv-database-logout-success-dbuser
  Product = Oracle Database
  Vendor = Oracle
  ParserVersion = "v1.0.0"
  TimeFormat = "M/d/yyyy H:mm:ss a"
  Conditions = [ """ AUDIT_TYPE=""", """ STATEMENT_TYPE=LOGOFF BY CLEANUP """, """ DB_USER=""" ]
  Fields = [
    """\sLOGOFF_TIME=({time}\d+\/\d+\/\d\d\d\d \d+:\d\d:\d\d (am|AM|pm|PM))""",
# audit_type is removed
    """\sSTATEMENT_TYPE=(|({reason}.+?))(\s+\w+=|\s*$)""",
    """\sOS_USER=(|({user}.+?))(\s+\w+=|\s*$)""",
    """\sDB_USER=(|({db_user}.+?))(\s+\w+=|\s*$)""",
    """\sUHOST=(|({host}.+?))(\s+\w+=|\s*$)""",
    """\sOBJECT_SCHEMA=(|({db_schema}.+?))(\s+\w+=|\s*$)""",
    """\sOBJECT_NAME=(|({db_name}.+?))(\s+\w+=|\s*$)""",
# comment_text is removed
    """\sSESSION_ID=({session_id}\d+)""",
    """\sOS_PROCESS=(|({process_id}.+?))(\s+\w+=|\s*$)""",
    """\sACTION=(|({action}.+?))(\s+\w+=|\s*$)"""
  ]


}
```