#### Parser Content
```Java
{
Name = microsoft-windows-xml-app-activity-success-10036
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - System
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """<EventID Qualifiers""", """<System><Provider Name""", """<TimeCreated SystemTime""", """<Computer>""", """<Channel>System<""", """>10036<""" ]
  Fields = [
    """<Computer>({host}[\w\.\-]+)<""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<TimeCreated SystemTime\\*=('|")?({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """<EventID Qualifiers\\*=('|")\d+('|")>({event_code}\d+)<\/EventID>""",
    """<Message>\s*({event_name}[^<]+?)\s*</Message>""",
    """<Keywords>({result}[^<]+)<\/Keywords>""",
    """<Task>({task}[^<]+)</Task>""",
    """<Execution ProcessID\\*=('|")({process_id}\d+)('|") ThreadID\\*=('|")({thread_id}\d+)('|")\/>""",
    """<EventData>({additional_info}.+?)<\/EventData>"""
    """Event Name:\s*({event_name}.+?)\s+\w+:"""
    """<Level>({run_level}[^<]+)<"""
  ]


}
```