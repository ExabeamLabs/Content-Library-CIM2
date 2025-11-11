#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-endpoint-login-fail-4625-1
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """CEF:""", """"eventID":"4625"""", """An account failed to log on""" ]
  Fields = [
    """"systemTime":"({time}\d+-\d+-\d+T\d+:\d+:\d+)""",
    """"computer":"({dest_host}({host}[\w\-.]+))""",
    """"message":"({event_name}[^"]+?)\s*"""",
    """"eventID":"({event_code}\d+)""",
    """"eventRecordID":"({event_id}\d+)""",
    """"severityValue":"({result}[^"]+?)\s*"""",
    """"status":"({failure_code}({result_code}[^"]+?))\s*"""",
    """"subStatus":"({failure_code}({result_code}[^"]+?))\s*"""",
    """"failureReason":"({failure_reason}[^"]+?)\s*"""",
    """"subjectUserSid":"({user_sid}[^"\s]+?)\s*"""",
    """"targetUserName":"({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*"""",
    """"targetDomainName":"({dest_domain}({domain}[^"\s]+?))\s*"""",
    """"subjectLogonId":"({login_id}[^"\s]+?)\s*"""",
    """"logonType":"({login_type}\d+?)\s*"""",
    """"logonProcessName":"({auth_process}[^"]+?)\s*"""",
    """"authenticationPackageName":"({auth_package}[^"]+?)\s*"""",
    """"workstationName":"({src_host_windows}({src_host}[\w\-\.]+?))\s*"""",
    """"ipAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"ipPort":"({src_port}\d+)""",
  ]


}
```