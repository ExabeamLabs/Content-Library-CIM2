#### Parser Content
```Java
{
Name = helpsystems-powertechiam-kv-process-create-success-sshfrom
  ParserVersion = v1.0.0
  Vendor = HelpSystems
  Product = Powertech Identity and Access Manager
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
"""sshd - ssh_runcmd""",
"""ssh from"""
  ]
  Fields = [
    """clientTime="*({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)Z"*""",
    """\d\dZ\s+({host}[\w\-.]+)\s+sshd - ssh_runcmd""",
    """user="*({user}[^"]+)"""",
    """touser="*({account}[^"]+)"""",
    """ssh from ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}) starting:""",
    """cmd="*({process_command_line}({path}({process_dir}(\/[^\/]+)*\/)({process_name}[^\/\s]+))\s*.*?)"+\] ssh from""",
    """({event_code}ssh_runcmd)"""
  ]
  DupFields = [ "host->dest_host", "process_guid->process_id", "path->process_path"]


}
```