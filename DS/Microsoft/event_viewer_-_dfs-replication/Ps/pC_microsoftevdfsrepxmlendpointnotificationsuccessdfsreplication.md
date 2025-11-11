#### Parser Content
```Java
{
Name = microsoft-evdfsrep-xml-endpoint-notification-success-dfsreplication
  Vendor = Microsoft
  Product = Event Viewer - DFS-Replication
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [  """<Channel>DFS Replication<""", """<Computer>""", """<Keywords>""", """<EventID""" ]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<Computer>({dest_host}({host}[\w\-.]+))""",
    """Provider Name\\*=('|")({provider_name}[^\'"]+)""",
    """Guid\\*=('|")\{({process_guid}[^\'"\}]+)""",
    """<EventRecordID>({event_id}.+?)<""",
    """<Keywords>({result_code}({result}[^<]+))""",
    """<EventID>({event_code}\d+)""",
    """<EventID Qualifiers='\d+'>({event_code}\d+)<""",
    """<EventData>({additional_info}.+?)<\/EventData>""",
    """<Execution ProcessID\\*=('|")({process_id}\d+)""",
    """<Task>({sub_category}[^<]+)""",
    """<Level>({run_level}[^<]+)<""",
    """<Channel>({channel}[^<]+)<"""
  ]
  ParserVersion = "v1.0.0"


}
```