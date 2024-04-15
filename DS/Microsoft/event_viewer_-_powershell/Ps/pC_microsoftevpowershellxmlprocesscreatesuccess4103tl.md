#### Parser Content
```Java
{
Name = "microsoft-evpowershell-xml-process-create-success-4103-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - PowerShell"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      "microsoft-windows-powershell"
      "context:"
      "<provider name="
      "<eventid>4103<"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime='({time}\\d+\\-\\d+\\-\\d+T\\d+:\\d+:\\d+\\.\\d{3})"
      "(?i)({event_code}4103)"
      "(?i)<Computer>({host}[^<>]+)</Computer>"
      "(?i)<Execution ProcessID='({process_id}\\d+)"
      "(?i)<Security UserID='({user_sid}[\\w\\-]+)'/>"
      "(?i)User = (({domain}[^\\\\]+?)\\\\)?({user}[^\\s]+)\\s+Connected User ="
      "(?i)CommandInvocation(.+?):\\s*\"({command_invocation}[^\"]+)"
      "(?i)value=\"*(?:function\\s)?({command_module}[^\\s\"]+)"
      "(?i)Host\\s*Application\\s*=\\s*({powershell_image}[^\\s]+)\\s+EngineVersion"
      "(?i)Host\\s*Application\\s*=\\s*({process_command_line}[^\\s]+)\""
      "(?i)CommandInvocation(.+?):\\s*\\\\*\"({command_invocation}[^\"]+)"
      "(?i)Details:.+?CommandInvocation.+?ParameterBinding.+?value=\"(function\\s)?({command_module}[^\\s,\"]+)"
      "(?i)Context[^@]+?User\\s*=\\s*(({domain}[^=]+?)[\\\\\\/]+)?(SYSTEM|({user}[^=\\/\\\\]+?))\\s*Connected User ="
      "(?i)Context[^@]+?Host Application\\s*=\\s*({process_command_line}.+?)\\s*Engine Version ="
      "(?i)Context[^@]+?Host Application\\s*=\\s*({process_path}(({process_dir}[^\\;=\\s]+)[\\\/]+)?({process_name}[^\\s]+)[^\\n]+?)\\s+Engine Version ="
      "(?i)Context[^@]+?Command Type\\s*=\\s*(|({command_type}[^=]+?))\\s*Script Name ="
      "(?i)Context[^@]+?Command Name\\s*=\\s*(|({command_name}[^=]+?))\\s*Command Type ="
      "(?i)Context[^@]+?Script Name\\s*=\\s+({script_name}\\S[^=]+?)\\s+Command Path ="
      "(?i)Engine Version\\s*=\\s*({engine_version}[^\\s]+)\\s*"
    ]
    DupFields = [
      "host->src_host"
    ]
    ParserVersion = "v1.0.0"
  

}
```