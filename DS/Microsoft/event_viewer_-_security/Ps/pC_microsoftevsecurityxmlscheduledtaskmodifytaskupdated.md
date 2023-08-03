#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-scheduled-task-modify-taskupdated
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """A scheduled task was updated""", """<UserId>""", """<Command>""", """<Arguments>"""]
  Fields = [
    """({event_name}A scheduled task was updated)""",
    """Account Name:\s*({user}[\w\.\-]{1,40}\$?)\s*Account Domain:\s*({domain}.+?)\s*Logon ID:\s*({login_id}.+?)\s*Task Information:""",
    """Task Name:\s*({task_name}.+?)\s*Task New""",
    """<UserId>({user_sid}[^<]+?)</UserId>""",
    """<RunLevel>({run_level}[^<]+?)</RunLevel>""",
    """<Triggers>\s*({triggers}.+?)\s*</Triggers>""",
    """<Command>({process_path}({process_dir}(?:(\w+:)?[^:<"]+?)?[\\\/]+)?({process_name}[^<"\\\/]+?))</Command>""",
    """<Arguments>({arg}[^<]+?)</Arguments>"""
  ]


}
```