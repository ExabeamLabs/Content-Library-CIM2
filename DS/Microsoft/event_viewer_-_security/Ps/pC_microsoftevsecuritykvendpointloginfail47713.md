#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-login-fail-4771-3
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """Kerberos Authentication Service""", """Microsoft-Windows-Security-Auditing""","""ServiceName:""", """TicketOptions:""", """4771"""]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\.\d{1,3}[+\-]+\d\d:\d\d""",
    """({host}[^\s]+)\s+Kerberos Authentication Service""",
    """({event_code}4771)""",
    """TargetUserName:({user}[\w\.\-\!\#\^\~]{1,40}\$?),""",
    """TargetSid:({user_sid}[^,]+),""",
    """ServiceName:\w+\/(?=\w)({domain}[^,]+)""",
    """Status:({result_code}[^,]+),""",
    """IpAddress:(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,""",
    """({result}(Success|Failure) Audit)"""
  ]
  DupFields = [ "result_code->failure_code", "user_sid->dest_user_sid", "user->dest_user" ]
  ParserVersion = "v1.0.0"


}
```