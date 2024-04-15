#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-user-create-success-4720-1-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>4720</eventid>"
      "a user account was created"
    ]
    Fields = [
      "(?i)({event_name}A user account was created)"
      "(?i)SystemTime=\\'({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[^<]+)</Computer>"
      "(?i)<EventID>({event_code}[^<]+)</EventID>"
      "(?i)Subject:.+?Account Name:\\s*({user}.+?)\\s*Account Domain:\\s*({domain}.+?)\\s*Logon ID:\\s*({login_id}.+?)\\s*New Account:"
      "(?i)New Account:.+?Security ID:\\s*({account_id}.+?)\\s*Account Name:\\s*({account_name}.+?)\\s*Account Domain:\\s*({account_domain}.+?)\\s*Attributes"
    ]
    DupFields = [
      "host->dest_host"
    ]
  

}
```