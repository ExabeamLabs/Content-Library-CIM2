#### Parser Content
```Java
{
Name = microsoft-sysmon-cef-log-success-servicestatechanged
  Vendor = Microsoft
  Product = Sysmon
  ParserVersion = v1.0.0
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|Microsoft Sysmon|Sysmon NXLog|""", """|SysmonTask-SYSMON_SERVICE_STATE_CHANGE|Sysmon service state changed|""" ]
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
    """\WdeviceSeverity=({severity}.+?)\s+(\w+=|$)""",
  ]
  DupFields = [ "host->dest_host" ]


}
```