#### Parser Content
```Java
{
Name = "microsoft-evapp-xml-app-activity-success-12288"
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Application
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """<EventID Qualifiers""",  """<Channel>Application<""", """>12288<""" ]
  Fields = [
    """<Computer>({host}[\w\.\-]+)<""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<TimeCreated SystemTime\\*=('|")?({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """<EventID Qualifiers\\*=('|")([\d]+)('|")>({event_code}\d+)<\/EventID>""",
    """<Message>\s*({event_name}[^<]+?)\s*</Message>""",
    """<Keywords>({result}[^<]+)<\/Keywords>""",
    """<Task>({task_name}[^<]+)</Task>""",
    """<Execution ProcessID\\*=('|")({process_id}\d+)('|") ThreadID.+?=('|")({thread_id}\d+)('|")\/>""",
    """<EventData>({additional_info}.+?)<\/EventData>"""
    """Event Name:\s*({event_name}.+?)\s+\w+:"""
    """<Level>({run_level}[^<]+)<"""
  ]


}
```