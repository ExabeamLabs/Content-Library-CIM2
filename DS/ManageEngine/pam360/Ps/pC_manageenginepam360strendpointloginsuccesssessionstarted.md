#### Parser Content
```Java
{
Name = manageengine-pam360-str-endpoint-login-success-sessionstarted
  ParserVersion = v1.0.0
  Conditions= [ """Session_Started""", """Success""", """RDP_initiated_from_PAM360_to_""" ]
  Fields = ${ManageEngineParserTemplates.pam360-app-activity.Fields}[
    """({event_name}Session_Started)""",
    """\sResourceAudit:({user}[^:]+):({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """RDP_initiated_from_PAM360_to_({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """ResourceAudit:({user}[^:]+):({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
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
```