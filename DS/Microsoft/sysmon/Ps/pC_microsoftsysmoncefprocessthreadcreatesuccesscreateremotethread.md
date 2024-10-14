#### Parser Content
```Java
{
Name = microsoft-sysmon-cef-process-thread-create-success-createremotethread
  Vendor = Microsoft
  Product = Sysmon
  ParserVersion = v1.0.0
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|Microsoft Sysmon|Sysmon NXLog|""", """|SysmonTask-SYSMON_CREATE_REMOTE_THREAD|CreateRemoteThread detected|""" ]
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
# sproc is removed
    """\Wdproc=({process_path}({process_dir}.*?)({process_name}[^\\]+?))\s+(\w+=|$)""",
# new_thread_id is removed
# start_address is removed
# start_module is removed
# src_process_guid is removed
# target_process_guid is removed
    """\Wdpid=({process_id}\d+)""",
  ]
  DupFields = [ "host->dest_host" ]


}
```