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
    """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wdpt=({dest_port}\d+)""",
    """\Wsrc=(0.0.0.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """\Wspt=({src_port}\d+)""",
    """\Wproto=({protocol}[^\s]+)""",
    """\Wcs2=\s*(|({server_group}.+?))\s*(\w+=|$)""",
    """\Wcs3=(|({service_name}.+?))\s*(\w+=|$)""",
    """\Wcs4=(|({app}.+?))\s*(\w+=|$)""",
    """\Wcs11="*(({domain}[^\\\s",]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"*\s*(\w+=|$)""",
    """\Wcs13=(|({db_name}.+?))\s*(\w+=|$)""",
    """\Wcs14=(|({db_schema}.+?))\s*(\w+=|$)""",
    """\Wcs18=(|({result_reason}.+?))\s*(\w+=|$)""",
  ]
  DupFields = [ "db_user->account" ]


}
```