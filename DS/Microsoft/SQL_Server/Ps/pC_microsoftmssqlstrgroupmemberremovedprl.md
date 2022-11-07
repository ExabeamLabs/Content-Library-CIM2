#### Parser Content
```Java
{
Name = microsoft-mssql-str-group-member-remove-dprl
  Vendor = Microsoft
  Product = SQL Server
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSSSSS"
  Conditions = [ """MSSQLSERVER""", """action_id:DPRL""", """statement:""", """database_principal_name:""", """permission_bitmask:""" ]
  Fields = [
    """event_time:({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+)""",
    """\d\d:\d\d:\d\d ({host}[^\s]+)\s\w+""",
    """session_id:({session_id}[^\s]+)""",
    """\saction_id:({db_operation}[^\s]+)""",
    """database_name:({db_name}[^\s]+)""",
    """schema_name:({db_schema}[^\s]+)""",
    """server_instance_name:({dest_host}[^\s]+)""",
    """object_name:({object}[^\s]+)""",
    """statement:\s*({db_query}((?i)(Select|alter|BACKUP|RESTORE|dbcc|drop)).+?)\s+additional_information:""",
    """additional_information:\s*({additional_info}.+?)\s+\w+:""",
# permission_bitmask is removed
    """object_id:({object_id}[^\s]+)""",
    """\starget_database_principal_name:({target}[^\s]+)""",
    """\starget_server_principal_name:([^\\]+\\)?({dest_user}[^\s]+)\starget_server_principal_sid:""",
    """\sdatabase_principal_name:([^\\]+\\)?({db_user}[^\s]+)\starget_server_principal_name:""",
    """\sserver_principal_name:((NT SERVICE|NT AUTHORITY|NT Service|({domain}[^\\]+))?\\)?((?i)system|({user}[^\s]+))\sserver_principal_sid:""",
# server_principal_id is removed
# db_principal_id is removed
# target_server_principal_id is removed
# sequence_group_id is removed
    """\sserver_principal_sid:({user_sid}[^\s]+)""",
    """\starget_server_principal_sid:({dest_user_sid}[^\s]+)""",
    """statement:.+?DROP MEMBER \[(({account_domain}[^\\]+)?\\)?({account_id}[^\]]+)\]"""
  ]
  ParserVersion = "v1.0.0"


}
```