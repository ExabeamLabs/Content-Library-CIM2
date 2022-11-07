#### Parser Content
```Java
{
Name = secureauth-login-leef-app-activity
  ParserVersion = "v1.0.0"
  Vendor = SecureAuth
  Product = SecureAuth Login
  TimeFormat = "MMM dd yyyy HH:mm:ss.SSS"
  Conditions = [ """LEEF:""", """|SecureAuth|""" ]
  Fields = [
    """devTime=({time}\w{3}\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d.\d\d\d)""",
    """ApplianceMachineName =({host}[^\s]+)""",
    """cat=({category}[^\s]+)""",
    """usrName =({user}[^\s]+)""",
    """src=({src_ip}[A-Fa-f:\d.]+)""",
    """dst=({dest_ip}[A-Fa-f:\d.]+)""",
    """url=({domain}[^\s]+)""",
    """DestinationSiteUrl=({url}[^\s]+)""",
    """UserAgent=(\s*|({user_agent}.+?))\sProductType""",
    """sev=({severity}\d+)""",
    """resource=({event_name}.+?)\s+(\w+=|$)""",
  ]


}
```