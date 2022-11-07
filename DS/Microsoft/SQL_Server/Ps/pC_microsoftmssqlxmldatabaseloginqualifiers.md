#### Parser Content
```Java
{
Name = microsoft-mssql-xml-database-login-qualifiers
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = SQL Server
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
"""<Event xmlns=""",
"""<Provider Name ='MSSQL""",
"""<Keyword>Audit """
  ]
  Fields = [
    """<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<Provider Name ='({db_name}[^']+)'""",
    """<Computer>({host}.+?)<\/Computer>""",
    """<EventData><Data>(({domain}[^\\\/<>]+?)[\\\/]+)?({user}[^\\\/]+?)</Data>""",
    """<Data>\s*\[CLIENT:\s*({src_ip}[a-fA-F\d.:]+)""",
    """<Computer>({src_host}.+?)<\/Computer>.*?<Data>\s*\[CLIENT:\s*[^\]]*?local machine""",
    """<Data>\s*\[CLIENT:\s*[^\]]*?local machine.*?\].*?<Computer>({src_host}.+?)<\/Computer>""",
    """Connection made using ({auth_package}[^.]+).""",
    """<EventID Qualifiers=[^>]+>({event_code}\d+)""",
    """<Keyword>({result}Audit.+?)</Keyword>""",
    """<Message>[^<>]*?Reason:\s*({failure_reason}[^.]+?)\."""
    """\sserver_principal_name:(({domain}[^\\]+)\\)?({user}[^\s]+)\sserver_principal_sid""",
    """database_name:({db_name}[^\s]+)""",
    """\Wserver_principal_name:(({domain}[^\\\/]+?)[\\\/])?({db_user}[^\\\/\s]+?)(\s+\w+:|\s*$)""",
    """\Waction_id:({db_operation}[^\s]+)""",
    """schema_name:({db_schema}[^\s]+)""",
    """\Wobject_name:({table_name}[^\s]+)""",
    """\Wstatement:(|-- network|Login failed.+?|Network error code.+?|({db_query}.+?))(\s+\w+:|\s*$)""",

  ]
  DupFields = [ "host->dest_host" ]


}
```