#### Parser Content
```Java
{
Name = "microsoft-evdnsserver-xml-process-create-success-800-1-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - DNSServer"
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<provider name='powershell"
      ">800</eventid>"
      "<computer>"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[^<]+)</Computer>"
      "(?i)UserId=({domain}[^\\\\]+)({user}[^\\s]+?)\\s+HostName"
      "(?i)({event_code}800)"
      "(?i)ScriptName =\\s*(|({process_path}({process_dir}([\\w:]+\\\\)?([^\\\\]+?\\\\)*?)({process_name}[^\\\\=]*?)))\\s+CommandLine"
      "(?i)HostApplication=\\s*({powershell_image}[^=]+?)\\s+EngineVersion="
      "(?i)CommandLine=\\s*({process_command_line}[^<]+?)\\s*<\\/Data>"
      "(?i)<Data>CommandInvocation[^<]{0,10000}value=\"+\\s*(|-|({command_module}.+?))\\s*\"\\s*<\\/Data>"
      "(?i)<Data>CommandInvocation[^:]+:\\s*\"+({command_invocation}[^\"]+)"
    ]
  

}
```