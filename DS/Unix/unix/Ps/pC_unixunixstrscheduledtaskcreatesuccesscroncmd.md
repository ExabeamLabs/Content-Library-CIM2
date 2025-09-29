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
"""\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)\) CMD""",
"""\sCMD\s+\(({task_name}[^"]+?\s*\)\s+?\]?)\s+""",
"""\sCMD\s+\(\s*({task_name}[^\)]+?)\s*(\)|")""",
"""\sCMD\s+\(\s*({process_command_line}.+?)\)\s*("|$)""",
"""\sCMD\s\(([\w\-]+\s)?({process_path}(\/[^\/\)\s]+?)+?[\/]({process_name}[^\/\)\s]+?))(\s|\))"""
"""\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
]
ParserVersion = "v1.0.0"


}
```