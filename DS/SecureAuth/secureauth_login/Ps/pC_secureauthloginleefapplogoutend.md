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
    """usrName =({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """processId=({process_id}\d+)""",
    """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """url=({domain}[^\s]+)""",
    """sev=({severity}\d+)""",
    """resource=({event_name}.+?)\s+(\w+=|$)""",
  ]


}
```