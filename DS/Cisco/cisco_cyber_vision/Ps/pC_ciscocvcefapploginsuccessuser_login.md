#### Parser Content
```Java
{
Name = cisco-cv-cef-app-login-success-user_login
  Vendor = Cisco
  Product = Cisco Cyber Vision
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSz"
  Conditions = [ """CEF:""", """|Cisco|Cyber Vision|""", """cat=Cisco Cyber Vision Operations""", """ cybervision[""", """user_login""" ]
  Fields = [
    """({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d{1,6}[+\-]\d\d:\d\d)\s({host}[\w\-\.]+)\scybervision""",
    """({app}Cyber Vision)""",
    """Cisco\|([^\|]+\|){2}({operation_type}[^\|]+)""",
    """Cisco\|([^\|]+\|){3}({event_name}[^\|]+)""",
    """\|cat=({category}[^=]+?)\s\w+=""",
    """\smsg=({additional_info}[^=]+?)\s\w+=""",
    """\ssuser=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  ]


}
```