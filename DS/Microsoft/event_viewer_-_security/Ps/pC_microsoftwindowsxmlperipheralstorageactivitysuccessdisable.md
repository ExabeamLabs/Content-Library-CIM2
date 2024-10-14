#### Parser Content
```Java
{
Name = "microsoft-windows-xml-peripheral-storage-activity-success-disable"
ParserVersion = "v1.0.0"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
Conditions = [
"""Microsoft-Windows-Security-Auditing"""
"""<EventID>6419</EventID>"""
]
Fields = [
"""<TimeCreated SystemTime\\*=('|")({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
"""<Computer>({dest_host}[\w\-.]+?)<\/Computer>"""
"""<Data Name\\*=('|")SubjectUserSid('|")>({user_sid}[^\<]+)<\/Data>"""
"""<Data Name(\\)?=('|")SubjectUserName('|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)<\/Data>"""
"""<Data Name\\*=('|")DeviceDescription('|")>({device_description}[^\<]+)<\/Data>"""
"""<Data Name\\*=('|")DeviceId('|")>({device_id}[^\<]+)<\/Data>"""
"""<Data Name\\*=('|")SubjectDomainName('|")>({domain}[^\<]+)<\/Data>"""
"""<Data Name\\*=('|")LocationInformation('|")>\s*(|-|({additional_info}[^\s]*?))\s*<\/Data>"""
"""<Data Name\\*=('|")ClassName('|")>\s*(|-|({device_class}[^\s]*?))<\/Data>"""
""">({event_code}6419)<\/EventID>"""
"""({event_name}A request was made to disable a device.)"""
"""<Level>({run_level}[^<]+)<"""
"""<Data Name ='DeviceId'>USB\\+VID_({device_vid}[^&]+)&(amp;)?PID_({device_pid}[^\\&]+)""""
]


}
```