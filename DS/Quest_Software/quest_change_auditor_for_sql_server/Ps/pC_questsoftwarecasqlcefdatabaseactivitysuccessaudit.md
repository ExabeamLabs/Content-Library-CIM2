#### Parser Content
```Java
{
Name = questsoftware-casql-cef-database-activity-success-audit
Vendor = Quest Software
Product = Quest Change Auditor for SQL Server
ParserVersion = "v1.0.0"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
Conditions = [ """|Quest Software Inc.|""", """|Change Auditor|""", """|SQL|""", """SQL|Audit """ ]
Fields = [
  """({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d+(\+|-)\d+:\d+)""",
  """\ssqlSessionLoginName =(({domain}NT AUTHORITY|[^\\\s]+)[\\]+)?({db_user}({user}SYSTEM|LOCAL SERVICE|ANONYMOUS LOGON|[\w\.\-\!\#\^\~]{1,40}\$?))""",
  """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
  """\sipAddress=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
  """\sdomain=({domain}[^\s]+)""",
  """\sshost=({src_host}[\w\-\.]+)""", 
  """\ssqlDatabaseName =({db_name}[^\s]+)""",
  """\smsg=({db_operation}[^=]+?)\s*\w+=""",
  """\ssqlObjectName =({db_object}[^\s]+)""",
  """\sdvchost=({dest_host}[\w\-\.]+)""",
  """\sdvchost=({host}[\w\-\.]+)""",
  """\ssqlTextData=({db_query}.*?)\s*\w+=""",
  """\ssqlApplicationName =({app}[^=]+?)\s*\w+="""
  """\ssqlInstanceName =({instance_id}[^\s]+)""" 
  ]


}
```