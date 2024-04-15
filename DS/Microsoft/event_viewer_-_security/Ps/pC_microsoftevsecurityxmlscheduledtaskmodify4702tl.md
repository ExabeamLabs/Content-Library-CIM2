#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-scheduled-task-modify-4702-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "MMM dd HH:mm:ss yyyy"
    Conditions = [
      "4702"
      "a scheduled task was updated"
    ]
    Fields = [
      "(?i)EventTime\":\"({time}\\d\\d\\d\\d-\\d\\d-\\d\\d \\d\\d:\\d\\d:\\d\\d)\""
      "(?i)<TimeCreated SystemTime='({time}\\d\\d-\\d\\d-\\d\\d\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d{3})"
      "(?i)({event_code}4702)"
      "(?i)({event_name}A scheduled task was updated)"
      "(?i)<Computer>({host}.+?)</Computer>"
      "(?i)({time}\\w+ \\d+ \\d+:\\d+:\\d+ \\d\\d\\d\\d)"
      "(?i):\\d+\\s({host}[^\\s]+)\\sMSWinEventLog"
      "(?i)<Keywords>({result}.+?)</Keywords>"
      "(?i)Security ID:\\s*(|({user_sid}[^:]+?))\\s*Account Name:\\s*(|({user}[^:]+?))\\s*Account Domain:\\s*(|({domain}[^:]+?))\\s*Logon ID:\\s*(|({login_id}[^:]+?))\\s*Task Information:"
      "(?i)Task Name:\\s*(|({task_name}.+?))\\s*Task New Content:"
      "(?i)(<|&lt;)UserId(>|&gt;)(?=\\w)(({account_domain}[^\\\\<]*)\\\\+)?({account_name}[^<]+)(<|&lt;)/UserId(>|&gt;)"
      "(?i)(<|&lt;)Settings(>|&gt;)\\s*({additional_info}.+?)\\s*(<|&lt;)/Settings(>|&gt;)"
      "(?i)(<|&lt;)Triggers(>|&gt;)\\s*({triggers}.+?)\\s*(<|&lt;)/Triggers(>|&gt;)"
      "(?i)(<|&lt;)RunLevel(>|&gt;)(?=\\w)({run_level}[^<]+)(<|&lt;)/RunLevel(>|&gt;)"
      "(?i)(<|&lt;)RegistrationInfo(>|&gt;).+?(<|&lt;)Author(>|&gt;)(?=\\w)({author}.+?)(<|&lt;)/Author(>|&gt;)"
      "(?i)(<|&lt;)RegistrationInfo(>|&gt;).+?(<|&lt;)Description(>|&gt;)(?=\\w)({description}.+?)(<|&lt;)/Description(>|&gt;)"
      "(?i)(<|&lt;)Command(>|&gt;)\"?({process_path}({process_dir}(?:(\\w+:)?[^:<\"]+?)?[\\\\\\/]+)?({process_name}[^<\"\\\\\\/]+?))(<|&lt;)/Command(>|&gt;)"
      "(?i)(<|&lt;)Arguments(>|&gt;)(\"+)?({arg}.+?)(<|&lt;)/Arguments(>|&gt;)"
    ]
    DupFields = [
      "host->dest_host"
    ]
  

}
```