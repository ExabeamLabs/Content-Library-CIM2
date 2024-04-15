#### Parser Content
```Java
{
Name = "microsoft-evdnsserver-xml-process-create-success-800-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - DNSServer"
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<provider name='powershell"
      "800</eventid>"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)\\.\\d+Z'/>"
      "(?i)<Computer>({host}[^<]+)</Computer>"
      "(?i)UserId=({domain}[^\\\\]+)(\\\\?)({user}[^\\s]+?)\\s+HostName"
      "(?i)Host\\s*Application\\s*=\\s*({powershell_image}[^\\s]+)\\s+EngineVersion"
      "(?i)ScriptName =\\s*(|({process_path}({process_dir}([\\w:]+\\\\)?([^\\\\]+?\\\\)*?)({process_name}[^\\\\=]*?)))\\s+CommandLine"
      "(?i)CommandLine=\\s*({process_command_line}[^<]+?)\\s*</Data>"
      "(?i)Details:.+?CommandInvocation.+?ParameterBinding.+?value=\\\\?\"(function\\s)?({command_module}[^\\s\\,\"]+)"
      "(?i)Details:.+?CommandInvocation\\(.+?\\):\\s*\\\\*\\\"({command_invocation}[^\\\"]+)"
      "(?i)({event_code}800)"
    ]
  

}
```