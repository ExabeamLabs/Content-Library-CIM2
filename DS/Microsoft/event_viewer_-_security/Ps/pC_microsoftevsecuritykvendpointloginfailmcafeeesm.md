#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-fail-mcafeeesm"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
  """|McAfee|ESM"""
  """43-26304771"""
]
Fields = [
  """({event_name}Kerberos pre-authentication failed)"""
  """\|McAfee\|[^|]+?\|[^|]+?\|43-2630({event_code}\d+)(0|1)\|"""
  """\srt=({time}\d{13})"""
  """shost=({host}[^\s]+)"""
  """src=(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """sntdom=({domain}[^\s]+)"""
  """suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+="""
  """nitroCommandID=({result_code}.+?)\s+\w+="""
]
DupFields = [
  "result_code->failure_code"
]
ParserVersion = "v1.0.0"


}
```