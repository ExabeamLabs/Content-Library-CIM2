#### Parser Content
```Java
{
Name = microsoft-evapp-kv-app-notification-success-1001
  Vendor = Microsoft
  Product = Event Viewer - Application
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """Event_ID="1001"""", """[Event.System""", """][Event.System.TimeCreated _SystemTime=""" ]
  Fields = [
    """Computer="({host}[^"]+)"""",
    """Event\.System\.TimeCreated _SystemTime="({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\d\d\dZ)"""",
    """Event\.System\.Provider\s_Name =["\\]+({event_name}[^"\\]+)["\\]+""",
    """Event_ID="({event_code}[^"]+)"""",
    """Keywords="({result}[^"]+)"""",
    """Attached files:\s+[^:]+\:\s+({file_path}[^\s]+\\({file_name}[^\s.]+(\.({file_ext}[^\s]+))?)?)"""
    """Event\sName:\s+({operation}[^\s]+)"""
  ]


}
```