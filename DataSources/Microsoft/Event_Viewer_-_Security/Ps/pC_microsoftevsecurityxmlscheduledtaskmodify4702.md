#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-scheduled-task-modify-4702
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """4702""", """A scheduled task was updated""" ]
  Fields = [
    """EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""",
    """<TimeCreated SystemTime='({time}\d\d-\d\d-\d\d\d\dT\d\d:\d\d:\d\d\.\d{3})""",
    """({event_code}4702)""",
    """({event_name}A scheduled task was updated)""",
    """<Computer>({host}.+?)</Computer>""",
    """({time}\w+ \d+ \d+:\d+:\d+ \d\d\d\d)""",
    """:\d+\s({host}[^\s]+)\sMSWinEventLog""",
    """<Keywords>({result}.+?)</Keywords>""",
    """Security ID:\s*(|({user_sid}[^:]+?))\s*Account Name:\s*(|({user}[^:]+?))\s*Account Domain:\s*(|({domain}[^:]+?))\s*Logon ID:\s*(|({login_id}[^:]+?))\s*Task Information:""",
    """Task Name:\s*(|({task_name}.+?))\s*Task New Content:""",
    """(<|&lt;)UserId(>|&gt;)(?=\w)(({account_domain}[^\\<]*)\\+)?({account_name}[^<]+)(<|&lt;)/UserId(>|&gt;)""",
    """(<|&lt;)Settings(>|&gt;)\s*({additional_info}.+?)\s*(<|&lt;)/Settings(>|&gt;)""",
    """(<|&lt;)Triggers(>|&gt;)\s*({triggers}.+?)\s*(<|&lt;)/Triggers(>|&gt;)""",
    """(<|&lt;)RunLevel(>|&gt;)(?=\w)({run_level}[^<]+)(<|&lt;)/RunLevel(>|&gt;)""",
    """(<|&lt;)RegistrationInfo(>|&gt;).+?(<|&lt;)Author(>|&gt;)(?=\w)({author}.+?)(<|&lt;)/Author(>|&gt;)""",
    """(<|&lt;)RegistrationInfo(>|&gt;).+?(<|&lt;)Description(>|&gt;)(?=\w)({description}.+?)(<|&lt;)/Description(>|&gt;)""",
    """(<|&lt;)Command(>|&gt;)"?({process_path}({process_dir}(?:(\w+:)?[^:<"]+?)?[\\\/]+)?({process_name}[^<"\\\/]+?))(<|&lt;)/Command(>|&gt;)""",
    """(<|&lt;)Arguments(>|&gt;)("+)?({arg}.+?)(<|&lt;)/Arguments(>|&gt;)"""
  ]
  DupFields = [ "host->dest_host" ]


}
```