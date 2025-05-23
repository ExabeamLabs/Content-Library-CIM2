#### Parser Content
```Java
{
Name = microsoft-mssql-xml-database-login-qualifiers
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = MSSQL
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
"""<Event xmlns=""",
"""<Provider Name =""",
"""MSSQL""",
"""<Keyword>Audit """
  ]
  Fields = [
    """<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<Provider Name =('|")({db_name}[^']+)('|")""",
    """<Computer>({dest_host}({host}[\w\-.]+?))<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<EventData><Data>(({domain}[^\\\/<>]+?)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>""",
    """<Data>\s*\[CLIENT:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """<Computer>({src_host}.+?)<\/Computer>.*?<Data>\s*\[CLIENT:\s*[^\]]*?local machine""",
    """<Data>\s*\[CLIENT:\s*[^\]]*?local machine.*?\].*?<Computer>({src_host}.+?)<\/Computer>""",
    """Connection made using ({auth_package}[^.]+).""",
    """<EventID Qualifiers=[^>]+>({event_code}\d+)""",
    """<Keyword>({result}Audit.+?)</Keyword>""",
    """<Message>[^<>]*?Reason:\s*({result_reason}[^.]+?)\."""
    """\sserver_principal_name:(({domain}[^\\\/:]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\sserver_principal_sid""",
    """database_name:({db_name}[^\s]+)""",
    """\Wserver_principal_name:(({domain}[^\\\/:]+?)[\\\/])?({db_user}[^\\\/\s]+?)(\s+\w+:|\s*$)""",
    """\Waction_id:({action}[^\s]+)""",
    """statement:[^:=]*\s*({db_operation}\b(Select|alter|BACKUP|RESTORE|dbcc|drop|CREATE|update|insert|delete|set|show|RECONFIGURE)\b).+?\s*additional_information:"""
    """schema_name:({db_schema}[^\s]+)""",
    """\Wobject_name:({table_name}[^\s]+)""",
    """<Level>({run_level}[^<]+)<"""
    """\Wstatement:(|-- network|Login failed.+?|Network error code.+?|({db_query}.+?))(\s+\w+:|\s*$)""",

  ]


}
```