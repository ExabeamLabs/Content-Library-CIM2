#### Parser Content
```Java
{
Name = unix-unix-kv-endpoint-activity-success-shellcmd
  ParserVersion = v1.0.0
  Conditions = [ """Command is """, """ -Line=""", """SHELL_CMD: """ ]
  Fields = ${DLUnixParsersTemplates.unix-events-1.Fields}[
    """({event_name}SHELL_CMD)""",
    """IPAddr=({src_ip}[a-fA-F:\d\.]+)""",
    """User=({user}[^;]+)""",
    """Command is ({process_command_line}[^$]+?)\s*$"""
  ]

unix-events-1 = {
  Vendor = Unix
  Product = Unix
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Fields = [
    """({time}\w+\s+\d+ \d\d:\d\d:\d\d \d\d\d\d)""",
    """\d\d:\d\d:\d\d(\.\S+)? \d\d\d\d ({host}[^\s]+)""",
  ]
  DupFields = [ "host->dest_host" 
}
```