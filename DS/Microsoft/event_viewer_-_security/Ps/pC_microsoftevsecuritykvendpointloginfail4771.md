#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-fail-4771"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSZ"
Conditions = [
  """Exabeam Windows 4771"""
  """summary_windows_4771_data"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+[+-]\d+)"""
  """({event_code}4771)"""
  """summary_windows_4771_data="+\d+:\d+:\d+\s*\d+-\d+-\d+:::({host}[^:::]+)?:::({event_code}[^:::]+)?:::({user_sid}[^:::]+)?:::({domain}[^:::]+)?:::(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)?:::([^:::]+):::({result_code}[^:::]+)?:::({user}[\w\.\-]{1,40}\$?)?""""
]
DupFields = [
  "host->dest_host"
  "result_code->failure_code"
]
ParserVersion = "v1.0.0"


}
```