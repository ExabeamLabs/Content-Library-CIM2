#### Parser Content
```Java
{
Name = manageengine-pam360-str-app-activity-success-sessionended
  ParserVersion = v1.0.0
  Conditions= [ """Session_Ended""", """Success""", """RDP_initiated_from_""", """has_stopped""" ]
  Fields = ${ManageEngineParserTemplates.pam360-app-activity.Fields}[
    """({operation}Session_Ended)""",
    """RDP_initiated_from_PAM360_to_({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """ResourceAudit:({user}[\w\.\-\!\#\^\~]{1,40}\$?):({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
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
    """LOGIN NAME\\?=(({email_address}[^@"]+@[^"\.]+.[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """DOMAIN NAME\\?=(-|({domain}[^\]]+))""",
    """IP\\?=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """ACTION_NAME\\?=(-|({event_name}[^\]]+))""",
    """STATUS\\?=({additional_info}[^\]]+)""",
    """({app}ADSSP)"""
  ]
 
}
```