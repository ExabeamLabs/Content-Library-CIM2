#### Parser Content
```Java
{
Name = "unix-unix-str-scheduled-task-create-success-cmd"
Vendor = "Unix"
Product = "Unix"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""" CMD """
"""]: ("""
""" CROND["""
]
Fields = [
    """\d\d:\d\d:\d\d(\.\S+)?\s({host}[^\s]+)""",
    """\w+\s+\d+\s+\d\d:\d\d:\d\d(\.\S+)?\s+({host}[\w\-.]+)""",
    """\((({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\) CMD""",
    """\sCMD\s+\(\s*({task_name}[^\)]+?)\s*\)""",
    """\sCMD\s+\(({task_name}[^"]+?\s*\)\s+\]?)\s+""",
    """\sCMD\s+\(({process_command_line}.+?)\)\s*("|$)""",
    """\sCMD\s\(([\w\-]+\s)?({process_path}(\/[^\/\)\s]+)+)(\s|\))"""
]
ParserVersion = "v1.0.0"


}
```