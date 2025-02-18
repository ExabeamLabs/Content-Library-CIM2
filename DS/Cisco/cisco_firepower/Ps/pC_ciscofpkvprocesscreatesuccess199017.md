#### Parser Content
```Java
{
Name = cisco-fp-kv-process-create-success-199017
  Vendor = "Cisco" 
  Product = "Cisco Firepower"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """%FTD-""", """-199017""", """COMMAND="""]
  Fields = [
    """({time}\w{3}\s+\d+\s+(\d+\s+)?\d\d:\d\d:\d\d)\s({host}[\w\-\.]+)\s:""",
    """%FTD-({priority}\d+)-({event_code}\d+)""",
    """\WUSER=(({email_address}[^;\s\)@\\\/]+@[^;\s\)@\\\/]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s"""
    """\WPWD\\?=({process_dir}[^\s;]+)""",
    """\WCOMMAND\\?=({process_command_line}[^\"]+)(\"|$|\s(?:|;|$))""",
  ]
  ParserVersion = v1.0.0  


}
```