#### Parser Content
```Java
{
Name = "microsoft-windows-xml-app-activity-success-10036-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Windows"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Conditions = [
      "<eventid qualifiers='"
      "<system><provider name="
      "<timecreated systemtime='"
      "<computer>"
      ">10036<"
    ]
    Fields = [
      "(?i)<Computer>({host}[\\w.-]+)<\\/Computer>"
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d\\-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d\\d\\d\\d\\d\\d\\dZ)'"
      "(?i)<EventID Qualifiers='\\d+'>({event_code}\\d+)<\\/EventID>"
      "(?i)<Message>\\s*({event_name}[^<]+?)\\s*</Message>"
      "(?i)<Keywords>({result}[^<]+)<\\/Keywords>"
      "(?i)<Task>({task}[^<]+)</Task>"
      "(?i)<Execution ProcessID='({process_id}\\d+)' ThreadID='({thread_id}\\d+)'\\/>"
    ]
  

}
```