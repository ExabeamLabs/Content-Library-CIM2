#### Parser Content
```Java
{
Name = microsoft-adfs-str-app-authentication-fail-413
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Active Directory Federation Services
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [  """ 413 """, """ An error occurred during processing of a token request""",""" MSWinEventLog """ ]
  Fields = [
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
     """({time}\w\w\w\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
     """({event_name}An error occurred during processing of a token request)"""
    """Caller:\s*(({domain}[^\\\s]+)\\+)?(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """Client IP:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  ]


}
```