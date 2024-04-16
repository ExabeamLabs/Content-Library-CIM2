#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-scheduled-task-modify-4702
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = ["MMM dd HH:mm:ss yyyy", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
  Conditions = [ """4702""", """A scheduled task was updated""" ]
  Fields = [
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}[\+\-]\d{1,2}:\d{1,2})\s({host}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-.]+))\s""",
    """EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""",
    """<TimeCreated SystemTime\\*=('|")({time}\d\d-\d\d-\d\d\d\dT\d\d:\d\d:\d\d\.\d{3})""",
    """({event_code}4702)""",
    """({event_name}A scheduled task was updated)""",
    """"Computer":"({host}({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-.]+))"""",
    """({time}\w+ \d+ \d+:\d+:\d+ \d\d\d\d)""",
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3}Z)""""
    """:\d+\s({host}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[^\s]+))\sMSWinEventLog""",
    """<Keywords>({result}.+?)</Keywords>""",
    """Security ID:\s*(|({user_sid}[^:]+?))\s*Account Name:\s*(|({user}[\w\.\-]{1,40}\$?))\s*Account Domain:\s*(|({domain}[^:]+?))\s*Logon ID:\s*(|({login_id}[^:]+?))\s*Task Information:""",
    """Task Name:\s*(|({task_name}.+?))\s*Task New Content:""",
    """(<|&lt;)UserId(>|&gt;)(?=\w)(({account_domain}[^\\<]*)\\+)?({account_name}[^<]+)(<|&lt;)/UserId(>|&gt;)""",
    """(<|&lt;)Settings(>|&gt;)\s*({additional_info}.+?)\s*(<|&lt;)/Settings(>|&gt;)""",
    """(<|&lt;)Triggers(>|&gt;)\s*({triggers}.+?)\s*(<|&lt;)/Triggers(>|&gt;)""",
    """(<|&lt;)RunLevel(>|&gt;)(?=\w)({run_level}[^<]+)(<|&lt;)/RunLevel(>|&gt;)""",
    """(<|&lt;)RegistrationInfo(>|&gt;).+?(<|&lt;)Author(>|&gt;)(?=\w)({author}.+?)(<|&lt;)/Author(>|&gt;)""",
    """(<|&lt;)RegistrationInfo(>|&gt;).+?(<|&lt;)Description(>|&gt;)(?=\w)({description}.+?)(<|&lt;)/Description(>|&gt;)""",
    """(<|&lt;)Command(>|&gt;)"?({process_path}({process_dir}(?:(\w+:)?[^:<"]+?)?[\\\/]+)?({process_name}[^<"\\\/]+?))(<|&lt;)/Command(>|&gt;)""",
    """(<|&lt;)Arguments(>|&gt;)("+)?({arg}.+?)(<|&lt;)/Arguments(>|&gt;)"""
    """<Level>({run_level}[^<]+)<"""
  ]


}
```