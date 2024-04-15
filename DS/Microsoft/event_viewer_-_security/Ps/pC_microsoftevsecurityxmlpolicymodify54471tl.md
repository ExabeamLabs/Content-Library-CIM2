#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-policy-modify-5447-1-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "5447"
      "microsoft-windows-security-auditing"
      "<data name='filtername'>"
    ]
    Fields = [
      "(?i)({event_name}Microsoft-Windows-Security-Auditing)"
      "(?i)({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[^<>]+)<\\/Computer>"
      "(?i)({event_code}5447)"
      "(?i)<Data Name ='UserName'>(({domain}[^\\\\]+)\\\\)?({user}[^<]+)<"
      "(?i)<Data Name ='UserSid'>({user_sid}[^<]+)<"
      "(?i)<Data Name ='ProcessId'>({process_id}[^<]+)<"
      "(?i)<Data Name ='LayerName'>({layer_name}[^<]+)<"
    ]
  

}
```