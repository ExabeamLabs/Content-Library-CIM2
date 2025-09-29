#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-notification-success-cron
  Vendor = Unix
  Product = Unix
  ParserVersion = "v1.0.0"
  TimeFormat = [ "yyyy-MM-dd HH:mm:ss", "MMM dd HH:mm:ss" ]
  Conditions = [ """cron[""", """]: """ ]
  Fields = [
    """\d\d:\d\d:\d\d(\.\S+)? (::ffff:)?({host}\S+)? f?cron\[""",
    """cron\[\d+\]:\s*({additional_info}.+?)\s*$"""
    """({time}\w{3}\s+\d+\s+\d\d:\d\d:\d\d)\s+(::ffff:)?({host}[\w\-.]+)""",
    """\(({account}[^\)]+?)\) CMD""",
    """\sCMD \(\s*({process_command_line}.+?)\)($|\s|")"""
    """\s+.*\/({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
  ]


}
```