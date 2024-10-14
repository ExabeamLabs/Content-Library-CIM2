#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-fail-4771-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
  """Kerberos pre-authentication failed"""
  """,4771,Microsoft-Windows-Security-Auditing"""
  """rsa_sa_log"""
]
Fields = [
  """({event_name}Kerberos pre-authentication failed)"""
  """(Mon|Tue|Wed|Thu|Fri|Sat|Sun) ({time}\w+ \d+ \d+:\d+:\d+ \d+)"""
  """Security,(rn=)?({event_id}[\d]+)"""
  """Failure Audit,({host}[^,]+)"""
  """\d{2}:\d{2}:\d{2} \d{4},({event_code}[^,]+),Microsoft-Windows-Security-Auditing"""
  """Account Information:\s+Security ID:\s+({user_sid}.+?)\s+Account"""
  """Account Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Service Information"""
  """Service Name:\s+\w+\/(?=\w)({domain}.+?)\s+Network Information"""
  """Client Address:\s+(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """Failure Code:\s+({result_code}[\w]+)"""
]
DupFields = [
  "result_code->failure_code"
]
ParserVersion = "v1.0.0"


}
```