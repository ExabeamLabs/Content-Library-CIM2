#### Parser Content
```Java
{
Name = microsoft-sysmon-xml-registry-rename-success-14
  Vendor = Microsoft
  Product = Sysmon
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """<EventID>14<""", """<Channel>Microsoft-Windows-Sysmon""", """Registry object renamed""" ]
  Fields = [
    """<TimeCreated SystemTime=['"]({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})""",
    """<EventID>({event_code}14)<""",
    """({event_name}Registry object renamed)""",
    """<Channel>({provider_name}Microsoft-Windows-Sysmon)""",
    """<Computer>({host}[\w\-.]+)<""",
    """<Data Name =['"]EventType['"]>({event_category}[^<]+)<""",
    """<Data Name =['"]ProcessId['"]>({process_id}\d+)<""",
    """<Data Name =['"]Image['"]>({process_path}({process_dir}[^<>]*?)({process_name}[^.\\\/<]+\.\w+))<""",
    """<Data Name =['"]User['"]>(({domain}[^\\<]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)<""",
    """<Data Name =['"]TargetObject['"]>({old_registry_details}[^<>]+)<""",
    """<Data Name =['"]NewName['"]>({registry_details}[^<>]+)<""",
    """<Data Name =['"]ProcessGuid['"]>\{({process_guid}[^\}<]+)\}<""",
    """<Data Name =['"]RuleName['"]>({rule}[^<]+)<""",
    """<Security UserID=['"]({user_sid}[^'"]+)['"]"""
  ]


}
```