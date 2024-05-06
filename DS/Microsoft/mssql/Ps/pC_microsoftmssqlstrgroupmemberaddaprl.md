#### Parser Content
```Java
{
Name = microsoft-mssql-str-group-member-add-aprl
  Vendor = Microsoft
  Product = MSSQL
  Conditions = [ """MSSQLSERVER""", """action_id:APRL""", """statement:""", """database_principal_name:""", """permission_bitmask:""" ]
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSSSSS"
  Fields = [
    """event_time:({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+)""",
    """\d\d:\d\d:\d\d ({host}[^\s]+)\s\w+""",
    """<Computer>({host}[\w\-.]+)<"""
    """session_id:({session_id}[^\\\s]+)""",
    """\saction_id:({db_operation}[^\s]+)""",
	  """[rnt\\]+action_id:({db_operation}[^\\\s]+)"""
    """database_name:({db_name}[^\\\s]+)""",
    """schema_name:({db_schema}[^\\\s]+)""",
    """server_instance_name:({dest_host}[^\\\s]+)""",
    """object_name:({object}[^\\\s]+)""",
    """statement:\s*({db_query}((?i)(Select|alter|BACKUP|RESTORE|dbcc|drop)).+?)[rnt\s\\]*additional_information:""",
    """additional_information:\s*({additional_info}[^\s\\]+)\s+\w+:""",
# permission_bitmask is removed
    """object_id:({object_id}[^\\\s]+)""",
    """target_database_principal_name:({target}[^\\\s]+)""",
    """\starget_server_principal_name:([^\\]+\\)?({dest_user}[^\s]+)\starget_server_principal_sid:""",
    """\sdatabase_principal_name:([^\\]+\\)?({db_user}[^\s]+)\starget_server_principal_name:""",
    """database_principal_name:({db_user}[^\\\s]+)"""
	"""\sserver_principal_name:((NT SERVICE|NT AUTHORITY|NT Service|({domain}[^\\]+))?\\)?((?i)system|({user}[\w\.\-]{1,40}\$?))\sserver_principal_sid:""",
	"""server_principal_name:((NT SERVICE|NT AUTHORITY|NT Service|({domain}[^\\]+))?\\\\)?((?i)system|({user}[\w\.\-]{1,40}\$?))[rnt\\]*server_principal_sid:"""

# server_principal_id is removed
# db_principal_id is removed
# target_server_principal_id is removed
# sequence_group_id is removed
    """[rnt\s]+server_principal_sid:({user_sid}[^\\\s]+)""",
    """target_server_principal_sid:({dest_user_sid}[^\\\s]+)""",
    """statement:.+?ADD MEMBER \[(({account_domain}[^\\]+)?\\)?({account_id}[^\]]+)\]"""
    """statement:.+?ADD MEMBER \[(({account_domain}[^\\]+)?\\)?({account_id}[^\]]+)\]((?-i)\\+[rnt])*"""
  ]
  ParserVersion = "v1.0.0"


}
```