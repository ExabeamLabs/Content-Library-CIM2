#### Parser Content
```Java
{
Name = microsoft-sysmon-cef-process-create-success-sysmoncreateprocess
  Vendor = Microsoft
  Product = Sysmon
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|Microsoft Sysmon|Sysmon NXLog|""", """|SysmonTask-SYSMON_CREATE_PROCESS|Process Create|""" ]
  Fields = [
    """CEF:([^\|]*\|){5}({operation}[^\|]+)""",
    """({host}\S+) CEF:""",
    """\Wdvc=({host}[A-Fa-f:\d]+)""",
    """\Wdvchost=({host}[\w\-.]+)""",
    """\Wrt=({time}\d+)""",
    """\WeventId=({event_code}\d+)""",
    """\WcategoryOutcome=\/({result}.+?)\s+(\w+=|$)""",
    """\Wdntdom=(NT AUTHORITY|({domain}\S+))""",
    """\Wduser=(SYSTEM|LOCAL|NETWORK SERVICE|({user}[^\s]+))""",
    """\Wsproc=({parent_process}({parent_process_dir}.*?)({parent_process_name}[^\\]+?))\s+(\w+=|$)""",
    """\Wdproc=(SYSTEM|FINANS|({process_path}({process_dir}.*?)({process_name}[^\\]+?)))\s+(\w+=|$)""",
    """\Wcs4=\{({parent_process_guid}[^\}]+)""",
    """\Wcs6=\{({process_guid}[^\}]+)""",
    """\Wdpid=({process_id}\d+)""",
    """\Wcs1=({process_command_line}.+?)\s+(\w+=|$)""",
    """\Wcs2=({parent_process_command_line}.+?)\s+(\w+=|$)""",
    """\WfileHash=({hash_md5}\S+)""",
  ]
  ParserVersion = "v1.0.0"


}
```