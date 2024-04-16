#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-peripheral-storage-insert-success-6416
Vendor = "Microsoft"
Product = "Event Viewer - Security"
Conditions = [
  """<EventID>6416</"""
  """Microsoft-Windows-Security-Auditing"""
]
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ","epoch"]
Fields = [
"""<TimeCreated SystemTime\\*=('|")({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{9}Z)('|")\/>"""
"""<Computer>({dest_host}[\w\-.]+?)<\/Computer>"""
"""<Data Name\\*=('|")SubjectUserSid('|")>({user_sid}[^\<]+)<\/Data>"""
"""<Data Name\\*=('|")DeviceDescription('|")>({device_name}[^\<]+)<\/Data>"""
"""<Data Name\\*=('|")DeviceId('|")>({device_id}[^\<]+)<\/Data>"""
"""<Data Name\\*=('|")SubjectDomainName('|")>({domain}[^\<]+)<\/Data>"""
"""<Data Name\\*=('|")LocationInformation('|")>\s*(|-|({additional_info}[^\s]*?))<\/Data>"""
"""<Data Name\\*=('|")ClassName('|")>\s*(|-|({device_type}[^\s]*?))<\/Data>"""
""">({event_code}6416)<\/EventID>"""
"""({event_name}A new external device was recognized by the system.)"""
"""<Level>({run_level}[^<]+)<"""
]
ParserVersion = "v1.0.0"
DupFields = [
"event_name->operation"
]


}
```