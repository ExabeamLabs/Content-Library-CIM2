#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-key-5061
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [""""EventID":5061""", """Cryptographic operation"""]
  Fields = [
    """"EventTime":({time}\d+)""",
    """"EventTime":\s*"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""",
    """({event_name}Cryptographic operation)""",
    """"HostName":"({host}[^"]+)"""",
    """({event_code}5061)""",
    """"SubjectUserSid":"({user_sid}[^"]+)"""",
    """"SubjectUserName":"({user}[\w\.\-]{1,40}\$?)"""",
    """"SubjectDomainName":"({domain}[^"]+)"""",
    """"SubjectLogonId":"({login_id}[^"]+)"""",
    """"SeverityValue":({severity}[^,]+)""",
    """"ProcessID":({process_id}\d+)""",
    """"ProviderName":"({provider_name}[^"]+)"""",
# algorithm_name is removed
    """"KeyName":"({key_name}[^"]+)"""",
    """"+Hostname"+:"+({host}[^"]+)"+""",
  ]


}
```