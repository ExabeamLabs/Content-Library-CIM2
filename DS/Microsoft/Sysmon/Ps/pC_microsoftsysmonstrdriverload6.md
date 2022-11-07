#### Parser Content
```Java
{
Name = microsoft-sysmon-str-driver-load-6
  Vendor = Microsoft
  Product = Sysmon
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """Event_ID="6"""", """[Event.System""", """][Event.System.TimeCreated _SystemTime=""" ]
  Fields = [
    """Computer="({host}[^"]+)"""",
    """Event\.System\.TimeCreated _SystemTime="({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\d\d\dZ)"""",
    """Event\.System\.Provider\s_Name ="({event_name}[^"]+)"""",
    """Event_ID="({event_code}[^"]+)"""",
    """Keywords="({result}[^"]+)"""",
    """ImageLoaded:\s+({file_path}[^\s]+\\({file_name}[^\s]+\.({file_ext}[a-zA-Z]+)))""",
    """Event\.System\.Execution\s_ProcessID="({process_id}[^"]+)""",
    """Task="({operation}[^"]+)""",
    """Event\.System\.Security\s*_UserID="({user_sid}[^"]+)"""
  ]


}
```