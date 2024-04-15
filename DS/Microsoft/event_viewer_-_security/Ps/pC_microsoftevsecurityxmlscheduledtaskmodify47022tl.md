#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-scheduled-task-modify-4702-2-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>4702<"
    ]
    Fields = [
      "(?i)<EventID>({event_code}\\d+)"
      "(?i)<TimeCreated SystemTime(\\\\)?='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[^<]+)"
      "(?i)<Data Name(\\\\)?='SubjectUserSid'>({user_sid}[^<]+)"
      "(?i)<Data Name(\\\\)?='SubjectUserName'>({user}[^<]+)"
      "(?i)<Data Name(\\\\)?='SubjectDomainName'>({domain}[^<]+)"
      "(?i)<Data Name(\\\\)?='SubjectLogonId'>({login_id}[^<]+)"
      "(?i)<Data Name(\\\\)?='TaskName'>({task_name}[^<]+)"
      "(?i)(<|&lt;)UserId(>|&gt;)(?=\\w)(({account_domain}[^\\\\<]*)\\\\)?({account_name}[^<]+)(<|&lt;)/UserId(>|&gt;)"
      "(?i)(<|&lt;)Settings(>|&gt;)\\s*({additional_info}.+?)\\s*(<|&lt;)/Settings(>|&gt;)"
      "(?i)(<|&lt;)Triggers(>|&gt;)\\s*({triggers}.+?)\\s*(<|&lt;)/Triggers(>|&gt;)"
      "(?i)(<|&lt;)RunLevel(>|&gt;)(?=\\w)({run_level}[^<]+)(<|&lt;)/RunLevel(>|&gt;)"
      "(?i)(<|&lt;)RegistrationInfo(>|&gt;).+?(<|&lt;)Author(>|&gt;)(?=\\w)({author}.+?)(<|&lt;)/Author(>|&gt;)"
      "(?i)(<|&lt;)RegistrationInfo(>|&gt;).+?(<|&lt;)Description(>|&gt;)(?=\\w)({event_name}.+?)(<|&lt;)/Description(>|&gt;)"
      "(?i)(<|&lt;)Command(>|&gt;)\"?({process_path}({process_dir}(?:(\\w+:)?[^:<\"]+?)?[\\\\\\/]+)?({process_name}[^<\"\\\\\\/]+?))(<|&lt;)/Command(>|&gt;)"
      "(?i)(<|&lt;)Arguments(>|&gt;)(\"+)?({arg}.+?)(<|&lt;)/Arguments(>|&gt;)"
    ]
  

}
```