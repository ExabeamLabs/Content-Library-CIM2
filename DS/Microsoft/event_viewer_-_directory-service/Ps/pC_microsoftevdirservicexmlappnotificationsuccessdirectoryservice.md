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
    """<EventID Qualifiers=('|")\d+('|")>({event_code}\d+)<""",
    """<EventData>({additional_info}.+?)<\/EventData>""",
    """<Execution ProcessID\\*=('|")({process_id}\d+)""",
    """<Task>({sub_category}[^<]+)""",
    """<Level>({run_level}[^<]+)<""",
    """<Channel>({channel}[^<]+)<"""
    """<Security UserID=('|")({user_sid}[^"'<]+)"""
    """Client IP address:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({src_port}\d+)"""
    """Identity the client attempted to authenticate as:\s*(({domain}[^\\]+)\\)?({user}ANONYMOUS LOGON|[\w\.\-\!\#\^\~]{1,40}\$?)"""
  ]
  DupFields = [ "result->result_code" ]
  ParserVersion = "v1.0.0"


}
```