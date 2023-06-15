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
    """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """suser=({user}[^\s@]+)\s+(\w+=|$)""",
    """suser=({email_address}[^\s@]+@[^\s@]+)\s+(\w+=|$)""",
    """act=({action}[^"]+?)"*\s+$""",
  ]


}
```