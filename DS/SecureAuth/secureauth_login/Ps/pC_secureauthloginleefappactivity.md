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
    """usrName =(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s\w+=""",
    """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """url=({domain}[^\s]+)""",
    """DestinationSiteUrl=({url}[^\s]+)""",
    """UserAgent=(\s*|({user_agent}.+?))\sProductType""",
    """sev=({severity}\d+)""",
    """resource=({event_name}.+?)\s+(\w+=|$)""",
  ]


}
```