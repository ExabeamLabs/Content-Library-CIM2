#### Parser Content
```Java
{
Name = microsoft-sysmon-xml-dns-request-success-query
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Sysmon
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [
"""<Provider Name"""
"""'Microsoft-Windows-Sysmon'""",
"""<EventID>22</EventID>""",
"""<Channel>Microsoft-Windows-Sysmon/Operational</Channel>""",
"""<Data Name"""
  ]
  Fields = [
    """<Data Name\\*='UtcTime'>({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)</Data>""",
    """<TimeCreated SystemTime\\*='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """<EventID>({event_code}\d+)</EventID>""",
    """<Computer>({host}.+?)</Computer>""",
    """<Security UserID\\*='({user_sid}.+?)'/>""",
    """(?i)<Data Name\\*='ProcessGuid'>\{({process_guid}[A-F0-9a-f-]+)\}</Data>""",
    """<Data Name\\*='ProcessId'>({process_id}\d+)</Data>""",
    """<Data Name\\*='QueryName'>({dns_query}.+?)\s*</Data>""",
    """<Data Name\\*='QueryResults'>({dns_response}.+?)\s*</Data>""",
    """<Data Name\\*='Image'>({process_path}(({process_dir}[^<]*)\\+)?({process_name}.+?))</Data>"""
  ]


}
```