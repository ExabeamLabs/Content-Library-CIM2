#### Parser Content
```Java
{
Name = microsoft-mssql-xml-database-login-audit
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = MSSQL
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
    """\[CLIENT:\s+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]
  DupFields = [ "host->dest_host" ]


}
```