#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-endpoint-login-fail-4771-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  ""","EventID":"4771","""
  """<Data Name"""
  """TargetSid"""
  """Kerberos pre-authentication failed"""
]
Fields = [
  """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """({event_code}4771)"""
  """"Activity":"({event_name}[^"]+)"""
  """"Computer":"({host}[\w\-.]+)""",
  """<Computer>({host}[\w\-.]+)<""",
  """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
  """<Data Name\\*=('|")TargetSid('|")>(?:NONE_MAPPED|({user_sid}[^<]+))</Data>"""
  """<Data Name\\*=('|")Status('|")>({result_code}[^<]+)</Data>"""
  """<Data Name\\*=('|")TargetUserName('|")>(?=\w)({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>"""
  """<Data Name\\*=('|")ServiceName('|")>\w+\/(?=\w)({domain}[^<]+)</Data>"""
  """<Data Name\\*=('|")IpAddress('|")>(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?</Data>"""
  """<Level>({run_level}[^<]+)<"""
]
DupFields = [
  "result_code->failure_code"
]
ParserVersion = "v1.0.0"


}
```