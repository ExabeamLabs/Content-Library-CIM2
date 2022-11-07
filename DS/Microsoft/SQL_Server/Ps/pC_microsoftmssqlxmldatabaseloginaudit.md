#### Parser Content
```Java
{
Name = microsoft-mssql-xml-database-login-audit
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = SQL Server
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
"""<Event xmlns=""",
"""<Provider Name ='MSSQL""",
"""<Keyword>Audit """,
"""<Binary>"""
  ]
  Fields = [
    """<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<EventID Qualifiers=[^>]+>({event_code}\d+)""",
    """<Provider Name ='({db_name}[^']+)'""",
    """<Computer>({host}[^<]+)<\/Computer>""",
    """<Message>({additional_info}[^<]+)""",
    """<Keyword>({result}Audit[^<]+)<\/Keyword>""",
    """<Message>.+?user\s'((({domain}[^\\']+)\\)?({user}[^']+))'""",
    """\[CLIENT:\s+({src_ip}[a-fA-F\d:\.]+)"""
  ]
  DupFields = [ "host->dest_host" ]


}
```