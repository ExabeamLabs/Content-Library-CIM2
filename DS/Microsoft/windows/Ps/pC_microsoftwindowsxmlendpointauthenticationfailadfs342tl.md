#### Parser Content
```Java
{
Name = "microsoft-windows-xml-endpoint-authentication-fail-adfs342-tl"
    Vendor = "Microsoft"
    Product = "Windows"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      "'ad fs'"
      "<eventid>342</eventid>"
      "token validation failed"
    ]
    Fields = [
      "(?i)SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d)"
      "(?i)<Computer>({host}[^\\<]+)<\\/Computer>"
      "(?i)<EventID>({event_code}[^\\<]+)<\\/EventID>"
      "(?i)<EventRecordID>({event_id}[^\\<]+)<\\/EventRecordID>"
      "(?i)ProcessID='({process_id}[^\\']+)"
      "(?i)ThreadID='({thread_id}[^\\']+)"
      "(?i)UserID='({user_id}[^\\']+)"
      "(?i)<\\/Data><Data>({email_address}[^\\s]+?)\\s*\\-({failure_reason}.+?)<\\/Data><Data>"
    ]
    ParserVersion = "v1.0.0"
  

}
```