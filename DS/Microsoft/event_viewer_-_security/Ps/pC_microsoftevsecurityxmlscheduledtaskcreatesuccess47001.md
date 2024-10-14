#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-scheduled-task-create-success-4700-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "epoch"]
Conditions = [
"""4700"""
"""A scheduled task was enabled"""
]
Fields = [
""""TimeCreated":"[\\\/]*Date\(({time}\d{13})"""
"""({time}\w{1,3}\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
"""\w{1,3}\s{1,2}\d{1,2}\s\d\d:\d\d:\d\d\s(::ffff:)?({host}[^\s]+)""",
"""<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""\srt=({time}\d{13})""",
"""<Computer>({host}[^<]+?)</Computer>"""
 """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
"""({event_code}4700)"""
"""({event_name}A scheduled task was enabled)"""
"""\sAccount Name:\s*(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*Account Domain:\s*(|({domain}[^:]+?))\s*Logon ID:\s*(|({login_id}[^:]+?))\s*Task Information:"""
"""Task Name:\s*({task_name}[^:]+?)\s*Task Content:"""
"""Task Content:\s*(|({additional_info}[^<]+?))\s*<"""
"""<Level>({run_level}[^<]+)<"""
]
ParserVersion = "v1.0.0"
DupFields = [ "host-> dest_host"]


}
```