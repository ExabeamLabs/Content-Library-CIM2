#### Parser Content
```Java
{
Name = microsoft-evsystem-xml-endpoint-activity-success-5859
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Microsoft WMI Log
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
"""<EventID>5859<""",
"""Microsoft-Windows-WMI-Activity"""
"""<Channel>Microsoft-Windows-WMI-Activity/Operational</Channel>"""
  ]
  Fields = [
    """SystemTime=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<EventID>({event_code}[^<]+)</EventID>""",
    """<Computer>({dest_host}({host}[\w\-.]+))</Computer>""",
    """<Execution ProcessID="({parent_process_id}\d+)""",
    """<Security UserID\\*=('|")({user_sid}[^'"]+)""",
    """({process_name}WMI)""",
    """<Level>({run_level}[^<]+)<""",
    """<ClientMachine>({src_host}[\w\-.]+)</ClientMachine>""",
    """<User>(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)<""",
    """<ClientProcessId>({process_id}\d+)</ClientProcessId>""",
    """<Operation>({additional_info}[^<]+)</Operation>""",
    """<ResultCode>({result_code}[^<]+)</ResultCode>""",
    """<Query>({query}[^<]+)</Query>"""
  ]


}
```