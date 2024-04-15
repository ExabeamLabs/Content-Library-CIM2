#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-user-unlock-success-4767-1-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>4767</eventid>"
      "a user account was unlocked"
    ]
    Fields = [
      "(?i)({event_name}A user account was unlocked)"
      "(?i)SystemTime=\\'({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[\\w\\-.]+)</Computer>"
      "(?i)<EventID>({event_code}\\d+)</EventID>"
      "(?i)Subject:.+?Account Name:\\s*({user}.+?)\\s*Account Domain:\\s*({domain}.+?)\\s*Logon ID:\\s*({login_id}.+?)\\s*Target Account:"
      "(?i)Target Account:\\s*Security ID:\\s*({user_sid}.+?)\\s*Account Name:\\s*({dest_user}.+?)\\s*Account Domain:\\s*({dest_domain}[^=<]+)\\s*<"
    ]
    DupFields = [
      "host->dest_host"
    ]
    ParserVersion = "v1.0.0"
  

}
```