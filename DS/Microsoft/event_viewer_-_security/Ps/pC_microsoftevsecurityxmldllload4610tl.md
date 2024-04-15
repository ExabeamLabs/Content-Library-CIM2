#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-dll-load-4610-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      ">4610<"
      "microsoft-windows-security-auditing"
      "<data name='authenticationpackagename'>"
    ]
    Fields = [
      "(?i)({event_name}An authentication package has been loaded by the Local Security Authority)"
      "(?i)({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({src_host}[^<>]+)<\\/Computer>"
      "(?i)({event_code}4610)"
      "(?i)ProcessID='({process_id}\\d+)'"
      "(?i)ThreadID='({thread_id}\\d+)'"
      "(?i)<Keyword>({result}[^<]+)<"
      "(?i)<Data Name ='AuthenticationPackageName'>({auth_package}[^<]+)<"
    ]
  

}
```