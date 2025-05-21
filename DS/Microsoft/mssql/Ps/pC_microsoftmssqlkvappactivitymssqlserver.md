#### Parser Content
```Java
{
Name = microsoft-mssql-kv-app-activity-mssqlserver
  ParserVersion = "v1.0.0"
  Conditions = [ """MSSQLSERVER""", """action_id:""", """statement:""", """database_principal_name:""", """permission_bitmask:""" ]
  Fields = ${DLMicrosoftParsersTemplates.microsoft-sql-events.Fields} [
    """<Computer>({host}[\w\-.]+)<"""
    """[rnt\\]+action_id:({db_operation}[^\\\s]+)"""
    """database_principal_name:({db_user}[^\\\s]+)"""
    """server_principal_name:((NT SERVICE|NT AUTHORITY|NT Service|({domain}[^\\]+))?\\\\)?((?i)system|({user}[\w\.\-\!\#\^\~]{1,40}\$?))[rnt\\]*server_principal_sid:"""
  ]

microsoft-sql-events {
  Vendor = Microsoft
  Product = MSSQL
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSSSSS"
  Fields = [
    """event_time:({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+)""",
    """\d\d:\d\d:\d\d ({host}[^\s]+)\s\w+""",
    """session_id:({session_id}[^\\\s]+)""",
    """\saction_id:({db_operation}[^\\\s]+)""",
    """database_name:({db_name}[^\\\s]+)""",
    """schema_name:({db_schema}[^\\\s]+)""",
    """server_instance_name:({dest_host}[^\\\s]+)""",
    """object_name:({object}[^\\\s]+)""",
    """statement:\s*({db_query}((?i)(Select|alter|BACKUP|RESTORE|dbcc|drop|CREATE|update|insert|delete|set|show)).+?)\s+additional_information:""",
    """additional_information:\s*({additional_info}[^\s\\]+)\s+\w+:""",
# permission_bitmask is removed
    """object_id:({object_id}[^\\\s]+)""",
    """\starget_database_principal_name:({target}[^\s]+)""",
    """\starget_server_principal_name:([^\\]+\\)?({dest_user}[^\s]+)\starget_server_principal_sid:""",
    """\sdatabase_principal_name:([^\\]+\\)?({db_user}[^\s]+)\starget_server_principal_name:""",
    """\sserver_principal_name:((NT SERVICE|NT AUTHORITY|NT Service|({domain}[^\\]+))?\\)?((?i)system|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\sserver_principal_sid:""",
# server_principal_id is removed
# db_principal_id is removed
# target_server_principal_id is removed
# sequence_group_id is removed
    """server_principal_sid:({user_sid}[^\\\s]+)""",
    """target_server_principal_sid:({dest_user_sid}[^\\\s]+)""",
    """client_ip:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]
 }

logrhythm-o365-app-activity = {
  Vendor = LogRhythm
  Product = LogRhythm
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Fields = [
    """\sTS=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """USER=(Unknown|({email_address}[^@\s]+@[^\s\.]+?\.[^\s]+?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^\s]+))?)\s+\w+=""",
    """DOMAIN=(|({domain}[^\s]+?))\s+\w+=""",
    """WORKLOAD=({app}[^=]+?)\s+\w+=""",
    """COMMAND=({event_name}[^=]+?)\s+\w+=""",
    """OBJECT=(Unknown \(Unknown\)|({object}[^=]+?))\s+\w+=""",
    """\sFILENAME=({file_name}[^=]+?(\.({file_ext}[^\s\=\.]+))?)\s+\w+=""",
    """SIP=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """USERAGENT=\s*(|({user_agent}[^\n]+?))\s*(\w+=|$)""",
    """ITEMTYPE=({file_type}[^=]+?)\s+\w+=""",
    """RESULTCODE=({result}[^=]+?)\s+\w+="""
  ]
  DupFields = [ "event_name->operation" 
}
```