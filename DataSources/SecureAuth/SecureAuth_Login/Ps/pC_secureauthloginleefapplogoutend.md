#### Parser Content
```Java
{
Name = secureauth-login-leef-app-logout-end
  ParserVersion = "v1.0.0"
  Vendor = SecureAuth
  Product = SecureAuth Login
  TimeFormat = "MMM dd yyyy HH:mm:ss.SSS"
  Conditions = [ """LEEF:""", """|SecureAuth|""", """resource=Session - End""" ]
  Fields = [
    """devTime=({time}\w{3}\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d.\d\d\d)""",
    """cat=({category}[^\s]+)""",
    """usrName =({user}[^\s]+)""",
    """processId=({process_id}\d+)""",
    """src=({src_ip}[A-Fa-f:\d.]+)""",
    """dst=({dest_ip}[A-Fa-f:\d.]+)""",
    """url=({domain}[^\s]+)""",
    """sev=({severity}\d+)""",
    """resource=({event_name}.+?)\s+(\w+=|$)""",
  ]


}
```