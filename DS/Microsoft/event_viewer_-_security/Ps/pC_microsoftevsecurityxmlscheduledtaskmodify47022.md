#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-scheduled-task-modify-4702-2
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """<EventID>4702<""" ]
  Fields = [
    """<EventID>({event_code}\d+)""",
    """<TimeCreated SystemTime(\\)?='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<Computer>({host}[^<]+)""",
    """<Data Name(\\)?='SubjectUserSid'>({user_sid}[^<]+)""",
    """<Data Name(\\)?='SubjectUserName'>({user}[^<]+)""",
    """<Data Name(\\)?='SubjectDomainName'>({domain}[^<]+)""",
    """<Data Name(\\)?='SubjectLogonId'>({login_id}[^<]+)""",
    """<Data Name(\\)?='TaskName'>({task_name}[^<]+)""",
    """(<|&lt;)UserId(>|&gt;)(?=\w)(({account_domain}[^\\<]*)\\)?({account_name}[^<]+)(<|&lt;)/UserId(>|&gt;)""",
    """(<|&lt;)Settings(>|&gt;)\s*({additional_info}.+?)\s*(<|&lt;)/Settings(>|&gt;)""",
    """(<|&lt;)Triggers(>|&gt;)\s*({triggers}.+?)\s*(<|&lt;)/Triggers(>|&gt;)""",
    """(<|&lt;)RunLevel(>|&gt;)(?=\w)({run_level}[^<]+)(<|&lt;)/RunLevel(>|&gt;)""",
    """(<|&lt;)RegistrationInfo(>|&gt;).+?(<|&lt;)Author(>|&gt;)(?=\w)({author}.+?)(<|&lt;)/Author(>|&gt;)""",
    """(<|&lt;)RegistrationInfo(>|&gt;).+?(<|&lt;)Description(>|&gt;)(?=\w)({event_name}.+?)(<|&lt;)/Description(>|&gt;)""",
    """(<|&lt;)Command(>|&gt;)"?({process_path}({process_dir}(?:(\w+:)?[^:<"]+?)?[\\\/]+)?({process_name}[^<"\\\/]+?))(<|&lt;)/Command(>|&gt;)""",
    """(<|&lt;)Arguments(>|&gt;)("+)?({arg}.+?)(<|&lt;)/Arguments(>|&gt;)"""
  ]


}
```