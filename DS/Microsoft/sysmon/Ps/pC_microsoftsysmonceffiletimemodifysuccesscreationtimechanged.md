#### Parser Content
```Java
{
Name = microsoft-sysmon-cef-file-time-modify-success-creationtimechanged
  Vendor = Microsoft
  Product = Sysmon
  ParserVersion = v1.0.0
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|Microsoft Sysmon|Sysmon NXLog|""", """|SysmonTask-SYSMON_FILE_TIME|File creation time changed|""" ]
  Fields = [
    """CEF:([^\|]*\|){5}({event_name}[^\|]+)""",
    """({host}\S+) CEF:""",
    """\Wdvc=({host}[A-Fa-f:\d]+)""",
    """\Wdvchost=({host}[\w\-.]+)""",
    """\Wrt=({time}\d{13})""",
    """\WeventId=({event_code}\d+)""",
    """\WcategoryOutcome=\/({result}.+?)\s+(\w+=|$)""",
    """\WcategorySignificance=\/({category_significance}.+?)\s+(\w+=|$)""",
    """\WcategoryBehavior=\/({category_behavior}.+?)\s+(\w+=|$)""",
# category_device_group is removed
# category_object is removed
# category_custom_format_field is removed
    """\WdeviceSeverity=({device_severity}.+?)\s+(\w+=|$)""",
    """\Wdproc=.+?USERS\\+({user}[\w\.\-]{1,40}\$?)""",
    """\Wdproc=({process_path}({process_dir}.*?)({process_name}[^\\]+?))\s+(\w+=|$)""",
    """\Wcs6=\{({process_guid}[^\}]+)""",
    """\Wdpid=({process_id}\d+)""",
    """\Wfname=({file_path}({file_dir}.*?)({file_name}[^\\.]+(\.({file_ext}[^\\.]+?))?))\s+(\w+=|$)""",
  ]
  DupFields = [ "host->dest_host" ]


}
```