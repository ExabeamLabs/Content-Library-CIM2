#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-endpoint-login-4776-1
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"event_id":4776""", """The computer attempted to validate the credentials for an account.""" ]
  Fields = [
    """({event_name}The (computer|domain controller) attempted to validate the credentials for an account)""",
    """"@timestamp"\s*:\s*"({time}[^"]+)"""",
    """"(?:winlog\.)?computer_name"+\s*:\s*"+({host}[\w\-.]+)"""",
    """"(?:winlog\.)?computer_name"+\s*:\s*"+[^\."]+\.({domain}[^"]+)""",
    """"event_id"\s*:\s*({event_code}\d+)""",
    """"event_data"\s*:\s*\{.*?"Workstation"\s*:\s*"(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|(?:(?!NULL)(\\*({src_host}[^\s"]+))))"""",
    """"event_data"\s*:\s*\{.*?"Status"\s*:\s*"({result_code}[\w\-]+)"""",
    """"TargetUserName"\s*:\s*"(?![^\s"@]+@[^\s"@]+)({user}[\w\.\-]{1,40}\$?)"""",
    """"TargetUserName"\s*:\s*"({email_address}[^@"]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)?(({user}[\w\.\-]{1,40}\$?)@({domain}[^\s"@]+))?"""",
    """"TargetUserName"\s*:\s*"({email_address}({user}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+)@({domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"""",
    """"(record_number|record_id)"\s*:\s*"*({event_id}\d+)""",
  ]
  DupFields = ["host->dest_host"]


}
```