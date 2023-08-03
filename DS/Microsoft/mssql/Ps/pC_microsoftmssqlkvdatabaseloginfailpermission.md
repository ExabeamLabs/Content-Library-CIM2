#### Parser Content
```Java
{
Name = microsoft-mssql-kv-database-login-fail-permission
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = MSSQL
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSSSSS"
  Conditions = [
"""MSSQLSERVER""",
"""action_id:LGIF""",
"""statement:""",
"""database_principal_name:""",
"""permission_bitmask:"""
  ]
  Fields = [
    """event_time:({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+)"""
    """\d\d:\d\d:\d\d ({host}[^\s]+)\s\w+"""
    """session_id:({session_id}[^\s]+)"""
    """\saction_id:({db_operation}[^\s]+)"""
    """database_name:({db_name}[^\s]+)"""
    """\sdatabase_principal_name:([^\\]+\\)?({db_user}[^\s]+)\starget_server_principal_name:"""
    """\sserver_principal_name:((NT SERVICE|NT AUTHORITY|NT Service|({domain}[^\\]+))?\\)?((?i)system|({user}[\w\.\-]{1,40}\$?))\sserver_principal_sid:"""
    """Reason:\s({failure_reason}[^\.]+)"""
    """server_instance_name:({dest_host}[^\s]+)"""
    """({event_name}LGIF)"""
    """statement:({additional_info}.+?)\sadditional_information:"""
  ]


}
```