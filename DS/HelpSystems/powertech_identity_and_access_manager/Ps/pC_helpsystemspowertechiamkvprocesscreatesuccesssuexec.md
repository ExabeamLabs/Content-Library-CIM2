#### Parser Content
```Java
{
Name = helpsystems-powertechiam-kv-process-create-success-suexec
  ParserVersion = v1.0.0
  Vendor = HelpSystems
  Product = Powertech Identity and Access Manager
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
"""suexec - suexec_ok""",
"""Successful suexec"""
  ]
  Fields = [
    """clientTime="*({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)Z"*""",
    """\d\dZ\s+({host}[\w\-.]+)\s+suexec - suexec_ok""",
    """user="*({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
    """touser="*({account}[^"]+)"""",
    """Successful suexec \(pid ({process_guid}\d+)\)""",
    """cmd="*({process_command_line}({path}({process_dir}(\/[^\/]+)*\/)({process_name}[^\/]+))\s*.*?)"+\] Successful suexec""",
    """({event_code}suexec)"""
  ]
  DupFields = [ "host->dest_host", "process_guid->process_id", "path->process_path" ]


}
```