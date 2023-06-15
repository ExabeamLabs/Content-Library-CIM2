#### Parser Content
```Java
{
Name = manageengine-pam360-str-app-login-success-userloggedin
  ParserVersion = v1.0.0
  Conditions= [ """User_Logged_in_-_AD""", """Success""" ]
  Fields = ${ManageEngineParserTemplates.pam360-app-activity.Fields}[
    """({operation}User_Logged_in_-_AD)""",
    """\sResourceAudit:({user}[^:]+):({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """RDP_initiated_from_PAM360_to_({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """Success\s[\w\-\.]+\s\-({user}[^:]+)""",
    """({app}PAM360)"""
]    


pam360-app-activity = {
  Vendor = ManageEngine
  Product = PAM360
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Fields = [
    """\w+\s+\d+\s+\d\d:\d\d:\d\d\s+({host}[\w\-.]+)""",
    """({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)""",
    """({result}Success)""",
    ]
 }

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