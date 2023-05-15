#### Parser Content
```Java
{
Name = manageengine-adssp-cef-app-login-fail-passwordlogin
  ParserVersion = v1.0.0
  Conditions= [ """CEF:0|ManageEngine|ADSSP|""", """dvchost""", """DATE_TIME""", """ACTION_NAME\=Password Login""" ]

adssp-events = {
  Vendor = ManageEngine
  Product = ADSSP
  TimeFormat = "epoch"
  Fields = [
    """TIME\\?=({time}\d{13})""",
    """dvchost=({host}[\w\-.]+)""",
    """LOGIN NAME\\?=(({email_address}[^@"]+@[^"\.]+.[^"]+)|({user}[^\s\]]+))""",
    """DOMAIN NAME\\?=(-|({domain}[^\]]+))""",
    """IP\\?=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """ACTION_NAME\\?=(-|({event_name}[^\]]+))""",
    """STATUS\\?=({additional_info}[^\]]+)""",
    """({app}ADSSP)"""
  ]
 
}
```