#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-endpoint-login-fail-4771-5
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """"EventID":4771""", """"Kerberos Authentication Service"""", """"SourceName":"Microsoft-Windows-Security-Auditing"""", """"ServiceName":""", """"TicketOptions":""" ]
  Fields = [
    """"EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """\d\d:\d\d:\d\d\s({host}[\w\-.]+)\sMicrosoft-Windows-Security-Auditing""",
    """"Hostname":"({host}[\w\-.]+)"""",
    """"EventID":({event_code}4771)""",
    """"TargetUserName":"({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """"TargetSid":"({dest_user_sid}({user_sid}[^"]+))"""",
    """"ServiceName":"\w+\/(?=\w)({domain}[^"]+)"""",
    """"ServiceName":"({service_name}[^"]+)"""",
    """"Status":"({failure_code}({result_code}[^"]+))"""",
    """"IpAddress":"(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"EventType":"({result}[^"]+)""""
    """({event_name}Kerberos pre-authentication failed)"""
  ]
  ParserVersion = "v1.0.0"


}
```