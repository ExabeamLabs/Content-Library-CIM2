#### Parser Content
```Java
{
Name = "unix-unix-str-scheduled-task-create-success-croncmd"
Vendor = "Unix"
Product = "Unix"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""") CMD ("""
""" CRON["""
"""]: ("""
]
Fields = [
"""\d\d:\d\d:\d\d(\.\S+)?\s({host}[^\s]+)""",
"""\w+\s+\d+\s+\d\d:\d\d:\d\d(\.\S+)?\s+(::ffff:)?({host}[\w\-.]+)""",
"""\(({user}[^\)]+)\) CMD""",
"""\sCMD\s+\(\s*({task_name}[^\)]+?)\s*\)""",
"""\sCMD\s+\(({task_name}[^"]+?\s*\)\s+?\]?)\s+""",
"""\sCMD\s+({process_command_line}.+?)\s*("|$)"""
]
ParserVersion = "v1.0.0"


}
```