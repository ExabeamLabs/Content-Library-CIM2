#### Parser Content
```Java
{
Name = "microsoft-evsystem-xml-endpoint-login-fail-5805-1-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - System"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Conditions = [
      "netlogon"
      "the session setup from the computer"
      "5805</eventid>"
    ]
    Fields = [
      "(?i)SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d+Z)"
      "(?i)<EventID Qualifiers='0'>({event_code}5805)<\\/EventID>"
      "(?i)<Computer>({host}[^<]+)<\\/Computer>"
      "(?i)<Message>({additional_info}[^<]+)<\\/Message>"
      "(?i)ComputerName(:|=)\\s*({host}[\\w.-]+)"
      "(?i)Event ID: ({event_code}\\d+)"
      "(?i)({event_name}The session setup from the computer ({src_host}[^\\s]+)\\sfailed to authenticate)"
      "(?i)The following error occurred:\\s+({failure_reason}[^<]+)\\.<\\/Message>"
    ]
    ParserVersion = "v1.0.0"
  

}
```