#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-policy-apply-fail-6145-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Conditions = [
      "<eventid>6145</eventid>"
      "<message>one or more errors occured while processing security policy in the group policy objects"
    ]
    Fields = [
      "(?i)<EventID>({event_code}\\d+)"
      "(?i)({event_name}One or more errors occured while processing security policy in the group policy objects)"
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d{9}Z)"
      "(?i)<Computer>({host}[^<]+)"
      "(?i)<Execution ProcessID='({process_id}\\d+)' ThreadID='({thread_id}\\d+)'"
      "(?i)<EventRecordID>({event_id}\\d+)"
      "(?i)<Data Name ='ErrorCode'>({error_code}\\d+)<\\/Data>"
      "(?i)<Keywords>({action}[^<]+)<\\/Keywords>"
      "(?i)<Opcode>({severity}[^<]+)<\\/Opcode>"
      "(?i)<Message>\\s*({additional_info}[^<]+?)\\s*<\\/Message>"
    ]
  

}
```