#### Parser Content
```Java
{
Name = safenet-thales-cef-app-authentication-auth
  Vendor = Safenet
  Product = Thales
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """CEF:""", """|Safenet|""", """|Authentication|Auth|""", """act=""", """AUTH_ATTEMPT""" ]
  Fields = [
    """({host}[\w\-.]+)\s+CEF:""",
    """src=({src_ip}[A-Fa-f:\d.]+)""",
    """suser=({user}[^\s@]+)\s+(\w+=|$)""",
    """suser=({email_address}[^\s@]+@[^\s@]+)\s+(\w+=|$)""",
    """act=({action}[^"]+?)"*\s+$""",
  ]


}
```