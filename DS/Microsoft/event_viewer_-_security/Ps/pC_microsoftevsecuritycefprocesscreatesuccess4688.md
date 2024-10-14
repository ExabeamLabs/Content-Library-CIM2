#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-process-create-success-4688
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "epoch"
  Conditions = [
"""|Microsoft-Windows-Security-Auditing:4688|""",
"""|A new process has been created.|"""
  ]
  Fields = [
    """({event_name}A new process has been created)""",
    """\Wrt=({time}\d{13})""",
    """\Wdhost=({host}[\w\-\.]+)\s*(\w+=|$)""",
    """\Wdvchost=({host}[\w\-\.]+)\s*(\w+=|$)""",
    """\Wdst=({dest_ip}[a-fA-F:\.\d]+)\s*(\w+=|$)""",
    """({event_code}4688)""",
    """\Wduser=(?:-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*(\w+=|$)""",
    """\Wdntdom=(?:-|({domain}[^\s]+))\s*(\w+=|$)""",
    """\WdeviceNtDomain=(?:-|({domain}[^\s]+))\s*(\w+=|$)""",
    """\Wdproc=({process_path}({process_dir}(?:[^"]+?)?[\\\/])?({process_name}[^\\\/]+?))\s*(\w+=|$)""",
    """\Wdproc=({path}.+?)\s*(\w+=|$)""",
    """\Wduid=({login_id}[^\s]+)\s*(\w+=|$)""",
    """\Wcs2=({operation_type}.+?)\s*(\w+=|$)""",
    """\Wcs3=({process_guid}[^\s]+)\s*(\w+=|$)""",
    """\Wcs4=({process_command_line}.+?)\s*(\w+=|$)""",
    """\Wcs4=\s*(|-|(sc|((?:[^"]+)?[\\\/])?sc.exe)\s*(?:\\*[\w.\-]+)?\s*create\s*({service_name}.+?))\s+binPath= ({process_path}({process_dir}(?:[^"]+?)?[\\\/])?({process_name}[^\\\/]+?))\s*(\w+=|$)""",
    """\Wcs5=({parent_process_guid}[^\s]+)\s*(\w+=|$)""",
    """\sfilePath=({parent_process_path}({parent_process_dir}(?:[^"]+?)?[\\\/])?({parent_process_name}[^\\\/]+?))\s*(\w+=|$)"""
  ]
  DupFields = [ "process_guid->process_id" , "host->src_host" ]


}
```