#### Parser Content
```Java
{
Name = unix-unix-kv-endpoint-activity-fail-shellcmdmatchfail
  ParserVersion = v1.0.0
  Conditions = [ """SHELL_CMD_MATCHFAIL: """, """-User=""", """IPAddr=""" ]
  Fields = ${DLUnixParsersTemplates.unix-events-1.Fields}[
    """({event_name}SHELL_CMD_MATCHFAIL)""",
    """User=({user}[^-]+)""",
    """IPAddr=({src_ip}[a-fA-F:\d\.]+);\s({additional_info}[^.]+)"""
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