#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-dll-load-4614-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Conditions = [
      ">4614<"
      "microsoft-windows-security-auditing"
      "<data name='notificationpackagename'>"
    ]
    Fields = [
      "(?i)({event_name}Microsoft-Windows-Security-Auditing)"
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d+Z)"
      "(?i)<Computer>({src_host}[^<>]+)<\\/Computer>"
      "(?i)({event_code}4614)"
      "(?i)ProcessID='({process_id}\\d+)'"
      "(?i)ThreadID='({thread_id}\\d+)'"
      "(?i)<Keyword>({result}[^<]+)<"
      "(?i)<Data Name ='NotificationPackageName'>({object}[^<]+)<"
      "(?i)({event_name}A notification package has been loaded by the Security Account Manager)"
    ]
  

}
```