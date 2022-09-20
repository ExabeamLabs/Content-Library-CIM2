#### Parser Content
```Java
{
Name = microsoft-sysmon-cef-driver-load-success-driverloaded
  Vendor = Microsoft
  Product = Sysmon
  ParserVersion = v1.0.0
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|Microsoft Sysmon|Sysmon NXLog|""", """|SysmonTask-SYSMON_DRIVER_LOAD|Driver loaded|""" ]
  Fields = [
    """CEF:([^\|]*\|){5}({event_name}[^\|]+)""",
    """({host}\S+) CEF:""",
    """\Wdvc=({host}[A-Fa-f:\d]+)""",
    """\Wdvchost=({host}[\w\-.]+)""",
    """\Wrt=({time}\d+)""",
    """\WeventId=({event_code}\d+)""",
    """\WcategoryOutcome=\/({result}.+?)\s+(\w+=|$)""",
    """\WcategorySignificance=\/({category_significance}.+?)\s+(\w+=|$)""",
    """\WcategoryBehavior=\/({category_behavior}.+?)\s+(\w+=|$)""",
# category_device_group is removed
# category_object is removed
# category_custom_format_field is removed
    """\WdeviceSeverity=({device_severity}.+?)\s+(\w+=|$)""",
    """\Wdproc=.+?USERS\\+({user}[^\s\\]+)""",
    """\Wdproc=({process_path}({process_dir}.*?)({process_name}[^\\]+?))\s+(\w+=|$)""",
# image_loaded is removed
    """\Wcs2=({signature}.+?)\s+(\w+=|$)""",
# signature_status is removed
    """\Wcs4=({signed}.+?)\s+(\w+=|$)""",
    """\WfileHash=({file_hash}\S+)""",
  ]
  DupFields = [ "host->dest_host" ]


}
```