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
"""<Provider Name =""",
"""MSSQL""",
"""<Keyword>Audit """,
"""<Binary>"""
  ]
  Fields = [
    """<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<EventID Qualifiers=[^>]+>({event_code}\d+)""",
    """<Provider Name =('|")({db_name}[^']+)('|")""",
    """<Computer>({dest_host}({host}[\w\-.]+))<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Message>({additional_info}[^<]+)""",
    """<Keyword>({result}Audit[^<]+)<\/Keyword>""",
    """<Level>({run_level}[^<]+)<"""
    """<Message>.+?user\s'((({domain}[^\\']+)\\)?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'""",
    """\[CLIENT:\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]


}
```