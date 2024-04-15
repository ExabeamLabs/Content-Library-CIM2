#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-driver-load-fail-5038-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      ">5038<"
      "microsoft-windows-security-auditing"
      "<data name='param1'>"
    ]
    Fields = [
      "(?i)({event_name}Code integrity determined that the image hash of a file is not valid)"
      "(?i)({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({src_host}[^<>]+)<\\/Computer>"
      "(?i)({event_code}5038)"
      "(?i)ProcessID='({process_id}\\d+)'"
      "(?i)ThreadID='({thread_id}\\d+)'"
      "(?i)<Keyword>({result}[^<]+)<"
      "(?i)<Data Name ='param1'>({additional_info}[^<]+)<"
      "(?i)Guid='({process_guid}.+?)'"
      "(?i)<Data Name ='param1'>({file_path}[^<]+)</Data>"
      "(?i)<Data Name ='param1'>[^<]+[\\\\\\/]+({file_name}(?:[^<\\\\\\/:]+?)(\\.({file_ext}\\w+))?|[^\\\\:<]+)</Data>"
      "(?i)<Data Name ='param1'>({file_dir}.+?)[\\\\\\/]+(?:[^\\\\\\/]+?)</Data>"
    ]
  

}
```