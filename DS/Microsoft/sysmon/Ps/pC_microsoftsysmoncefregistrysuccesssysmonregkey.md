#### Parser Content
```Java
{
Name = microsoft-sysmon-cef-registry-success-sysmonregkey
  Vendor = Microsoft
  Product = Sysmon
  ParserVersion = v1.0.0
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|Microsoft Sysmon|Sysmon NXLog|""", """|SysmonTask-SYSMON_REG_KEY|Registry object added or deleted|""" ]
  Fields = [
    """CEF:([^\|]*\|){5}({event_name}[^\|]+)""",
    """({dest_host}({host}\S+)) CEF:""",
    """\Wdvc=({dest_host}({host}[A-Fa-f:\d]+))""",
    """\Wdvchost=({dest_host}({host}[\w\-.]+))""",
    """\Wrt=({time}\d{13})""",
    """\WeventId=({event_code}\d+)""",
    """\WcategoryOutcome=\/({result}.+?)\s+(\w+=|$)""",
    """\WcategorySignificance=\/({category_significance}.+?)\s+(\w+=|$)""",
    """\WcategoryBehavior=\/({category_behavior}.+?)\s+(\w+=|$)""",
# category_device_group is removed
# category_object is removed
# category_custom_format_field is removed
    """\WdeviceSeverity=({severity}.+?)\s+(\w+=|$)""",
    """\Wdproc=({process_path}({process_dir}.*?)({process_name}[^\\]+?))\s+(\w+=|$)""",
    """\Wdproc=({file_path}({file_dir}.*?)({file_name}[^\\.]+(\.({file_ext}[^\\.]+?))?))\s+(\w+=|$)""",
    """\Wcs6=\{({process_guid}[^\}]+)""",
    """\Wdpid=({process_id}\d+)""",
    """\Wcs1=({object}\S+)""",
  ]


}
```