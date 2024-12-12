#### Parser Content
```Java
{
Name = microsoft-evdirservice-xml-app-notification-success-directoryservice
  Vendor = Microsoft
  Product = Event Viewer - Directory-Service
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [  """<Channel>Directory Service<""", """<Computer>""", """<Keywords>""", """<EventID""" ]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<Computer>({host}[\w\-.]+)""",
    """Provider Name\\*=('|")({provider_name}[^\'"]+)""",
    """Guid\\*=('|")\{({process_guid}[^\'"\}]+)""",
    """<EventRecordID>({event_id}.+?)<""",
    """<Keywords>({result}[^<]+)""",
    """<EventID>({event_code}\d+)""",
    """<EventID Qualifiers='\d+'>({event_code}\d+)<""",
    """<EventData>({additional_info}.+?)<\/EventData>""",
    """<Execution ProcessID\\*=('|")({process_id}\d+)""",
    """<Task>({sub_category}[^<]+)""",
    """<Level>({run_level}[^<]+)<""",
    """<Channel>({channel}[^<]+)<"""
  ]
  DupFields = [ "result->result_code" ]
  ParserVersion = "v1.0.0"


}
```