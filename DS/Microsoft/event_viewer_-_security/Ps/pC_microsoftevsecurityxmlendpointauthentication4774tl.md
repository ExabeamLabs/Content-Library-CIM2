#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-endpoint-authentication-4774-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      "<eventid>4774</eventid>"
      "<task>credential validation"
      "an account was mapped for logon"
    ]
    Fields = [
      "(?i)({event_name}An account was mapped for logon)"
      "(?i)<TimeCreated SystemTime='({time}\\d{4}-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d)\\d+Z'\\/>"
      "(?i)<Computer>({host}[^<>]+)<\\/Computer>"
      "(?i)<EventID>({event_code}[^<]+)<\\/EventID>"
      "(?i)Account UPN:\\s*(?:({user_type}host)/)?(({domain}[^\\\\]+)\\\\+)?({user}[^\\s\\\\\\/]+)"
      "(?i)Mapped Name:\\s*({account}[^\\s\\<]+)"
    ]
  

}
```