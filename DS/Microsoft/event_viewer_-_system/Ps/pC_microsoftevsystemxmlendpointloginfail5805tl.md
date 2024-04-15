#### Parser Content
```Java
{
Name = "microsoft-evsystem-xml-endpoint-login-fail-5805-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - System"
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [
      "netlogon"
      "\"eventid\":5805"
      "failed to authenticate"
    ]
    Fields = [
      "(?i)\"EventID\"*:({event_code}[^,]+)"
      "(?i)\"EventTime\"*:\"*({time}\\d\\d\\d\\d-\\d\\d-\\d\\d\\s\\d\\d:\\d\\d:\\d\\d)\""
      "(?i)\"Hostname\"*:\"*({host}[^\"]+)\""
      "(?i)\"EventType\"*:\"*({result}[^\"]+)"
      "(?i)\"Domain\"*:\"*({domain}[^\"]+)"
      "(?i)\"Severity\"*:\"*({severity}[^\"]+)\""
      "(?i)\"SeverityValue\"*:({severity}[^,]+)"
      "(?i)\"AccountName\"*:\"*({user}[^\"]+)\""
      "(?i)\"SubjectUserSid\"*:\"*({user_sid}[^\"]+)\""
      "(?i)\"SubjectUserName\"*:\"*({user}[^\"]+)\""
      "(?i)\"SubjectDomainName\"*:\"*({domain}[^\"]+)\""
      "(?i)\"LogonID\"*:\"*({login_id}[^\"]+)\""
      "(?i)\"ProcessId\"*:\"*(\\\\t)*({process_id}[^\\\\]+)\""
      "(?i)\"Category\"*:\"*({event_name}[^\"]+)"
      "(?i)\"Message\"*:\"*({event_name}[^.]+)"
      "(?i)\"Message\"*:\"*The session setup from the computer ({src_host}[^\\s]+)\\s"
      "(?i)The following error occurred:(\\s|\\\\r|\\\\n)*({failure_reason}[^.\"]+)"
    ]
    ParserVersion = "v1.0.0"
  

}
```