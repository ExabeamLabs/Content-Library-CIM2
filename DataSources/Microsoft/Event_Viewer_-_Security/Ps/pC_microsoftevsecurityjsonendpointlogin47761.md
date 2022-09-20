#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-endpoint-login-4776-1
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"event_id":4776""", """The computer attempted to validate the credentials for an account.""", """"@timestamp"""" ]
  Fields = [
    """({event_name}The (computer|domain controller) attempted to validate the credentials for an account)""",
    """"@timestamp"\s*:\s*"({time}[^"]+)"""",
    """"(?:winlog\.)?computer_name"+\s*:\s*"+({host}[^"]+)"""",
    """"event_id"\s*:\s*({event_code}\d+)""",
    """"event_data"\s*:\s*\{.*?"Workstation"\s*:\s*"(({dest_ip}[A-Fa-f:\d.]+)|(?:(?!NULL)(\\*({dest_host}[^\s"]+))))"""",
    """"event_data"\s*:\s*\{.*?"Status"\s*:\s*"({result_code}[\w\-]+)"""",
    """"TargetUserName"\s*:\s*"(?![^\s"@]+@[^\s"@]+)({user}[^\s@"]+)"""",
    """"TargetUserName"\s*:\s*"(?=[^\s]+@[^\s]+)({email_address}({user}[^\s"@]+)@({domain}[^\s"@]+))"""",
    """"(record_number|record_id)"\s*:\s*"*({event_id}\d+)""",
  ]


}
```