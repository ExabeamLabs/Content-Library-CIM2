#### Parser Content
```Java
{
Name = pan-gp-cef-vpn-login-success-loginuserid
  Vendor = Palo Alto Networks
  Product = GlobalProtect
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [ """globalprotect """, """|login|USERID|""" ]
  Fields = [
    """end=({time}\d{4}\/\d{2}\/\d{2}\s(\d{2}:){2}\d{2})\s""",
    """src=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """({event_name}login)""",
    """duser=(({domain}[^\\\s,]+)\\+)?({user}[^\\\s,]+)""",
    """dvchost=({src_host}[\w.-]+?)\s""",
    """GPStatus=({result}\S+?)\s"""
  ]


}
```