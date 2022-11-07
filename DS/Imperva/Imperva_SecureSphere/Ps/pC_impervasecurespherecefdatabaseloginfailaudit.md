#### Parser Content
```Java
{
Name = imperva-securesphere-cef-database-login-fail-audit
  ParserVersion = v1.0.0
  Vendor = Imperva
  Product = Imperva SecureSphere
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ 
"""|Imperva Inc.|SecureSphere|"""
"""cs6=Login"""
"""cs8=False"""
]
  Fields = [
    """\Wrt=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d)""",
    """\Wcs12=(({domain}[^\\\s]+)\\+)?({host}[\w\-.]+)""",
    """\Wduser=(({domain}[^\\\s]+)\\+)?({db_user}[^\s]+)""",
    """\Wdst=({dest_ip}[A-Fa-f:\d.]+)""",
    """\Wdpt=({dest_port}\d+)""",
    """\Wsrc=(0.0.0.0|({src_ip}[A-Fa-f:\d.]+))""",
    """\Wspt=({src_port}\d+)""",
    """\Wproto=({protocol}[^\s]+)""",
    """\Wcs2=\s*(|({server_group}.+?))\s*(\w+=|$)""",
    """\Wcs3=(|({service_name}.+?))\s*(\w+=|$)""",
    """\Wcs4=(|({app}.+?))\s*(\w+=|$)""",
    """\Wcs11="*(({domain}[^\\\s",]+)\\+)?({user}[^\\\s",]+)"*\s*(\w+=|$)""",
    """\Wcs13=(|({db_name}.+?))\s*(\w+=|$)""",
    """\Wcs14=(|({db_schema}.+?))\s*(\w+=|$)""",
    """\Wcs18=(|({failure_reason}.+?))\s*(\w+=|$)""",
  ]
  DupFields = [ "db_user->account" ]


}
```