#### Parser Content
```Java
{
Name = eset-es-leef-app-logout-success-domainuserlogout
  ParserVersion = v1.0.0
  Vendor = ESET
  Product = ESET Endpoint Security
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ "LEEF:1.0|ESET|RemoteAdministrator|", """cat=ESET""", """|Domain user logout|""" ]
  Fields = [
    """\Wcat=({category}[^=]+?)\s*(\w+=|$)""",
    """\Wsev=({alert_severity}\d+)""",
    """\WdevTime=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d)""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Waction=({operation}[^\s]+)\s""",
    """\Wresult=({result}[^=]+?)\s*(\w+=|$)""",
    """\WdeviceName =({host}[^\s]+)\s""",
    """\Wtarget=({object}[^\s]+)\s*""",
    """\Wdetail=({additional_info}[^.]+).""",
    """\Wuser '\w+\\({user}[\w\.\-]{1,40}\$?)'.""",
    """(\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\|({event_name}[^|]+)\|""",
    """\d+Z\s*({host}\w+)\s""",
    """\Wuser=((NT AUTHORITY|({domain}[^\\=]+?))\\+)?(SYSTEM|({user}[^=\s]+?))\s*(\w+=|$)""",
  ]


}
```