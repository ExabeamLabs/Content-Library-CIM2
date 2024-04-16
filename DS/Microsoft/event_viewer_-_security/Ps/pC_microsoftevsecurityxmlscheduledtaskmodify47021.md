#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-scheduled-task-modify-4702-1
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """<EventID>4702<""", """A scheduled task was updated""", """&lt;Settings&gt;""" ]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{9}Z)""",
    """({event_code}4702)""",
    """({event_name}A scheduled task was updated)""",
    """<Computer>({src_host}({host}[^<]+))""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Keywords>({result}.+?)</Keywords>""",
    """Security ID:\s*({user_sid}.+?)\s*Account Name:\s*({user}[\w\.\-]{1,40}\$?)\s*Account Domain:\s*({domain}.+?)\s*Logon ID:\s*({login_id}.+?)\s*Task Information:""",
    """Task Name:\s*({task_name}.+?)\s*Task New""",
    """&lt;UserId&gt;(({account_domain}[^\\&]*)\\)?({account_name}[^&]+)&lt;/UserId&gt;""",
    """&lt;RunLevel&gt;({run_level}[^&]+)&lt;/RunLevel&gt;""",
    """&lt;Author&gt;(?=\w)({author}.+?)&lt;/Author&gt;""",
    """&lt;Description&gt;(?=\w)({description}.+?)&lt;/Description&gt;""",
    """&lt;Command&gt;"?({process_path}({process_dir}(?:(\w+:)?[^:&"]+?)?[\\\/]+)?({process_name}[^&"\\\/]+?))&lt;/Command&gt;""",
    """&lt;Arguments&gt;({arg}.+?)&lt;/Arguments&gt;"""
    """<Triggers>\s*(|({triggers}[^<]+))<"""
    """<Level>({run_level}[^<]+)<"""
  ]


}
```