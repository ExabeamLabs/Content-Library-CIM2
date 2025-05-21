#### Parser Content
```Java
{
Name = "microsoft-evsystem-xml-endpoint-activity-success-capi2-1"
  Conditions = [ """<Provider Name ="Microsoft-Windows-CAPI2"""", """<Execution ProcessID=""", """<EventID>""" ]
  Vendor = "Microsoft"
  Product = "Event Viewer - CAPI2"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Fields = [
    """Guid=('|")\{({process_guid}[^}]+?)\}"""
    """<TimeCreated SystemTime=('|")({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d.\d+Z)"""
    """<EventID>({event_code}\d+)</EventID>"""
    """<Task>({operation}.*?)</Task>"""
    """<Execution ProcessID\\*=('|")({process_id}\d+)"""
    """<Computer>({dest_host}({host}[\w\-.]+?))</Computer>"""
    """<Security UserID\\*='({user_sid}[^']+)'"""
    """<Keywords>({result}.+?)<\/Keywords>"""
    """<Level>({run_level}[^<]+)<"""
    """<Channel>({channel}[^<]+)<\/Channel>"""
    """ThreadID(\\)?=('|")({thread_id}\d+)"""
    """<EventAuxInfo(?:\s*|.*)ProcessName =["']({process_name}.*?)["'](?:.*)"""
  ]
  ParserVersion = "v1.0.0"


}
```