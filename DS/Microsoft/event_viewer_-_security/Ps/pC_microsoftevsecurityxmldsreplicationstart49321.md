#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-ds-replication-start-4932-1
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """<EventID>4932</EventID>""", """<Data Name""" ,"""<Execution ProcessID"""]
  Fields = [
    """<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<EventID>({event_code}\d+)""",
    """<Computer>({host}[^<]+)""",
    """<Execution ProcessID='({process_id}\d+)""",
    """<Task>({sub_category}[^<]+)""",
    """<Keywords>({result}[^<]+)""",
    """<Data Name ='DestinationDRA'>.+?CN=({dest_dra}[^<]+)""",
    """<Data Name ='SourceDRA'>({src_dra}[^<]+)<""",
    """<Data Name ='SessionID'>({session_id}\d+)<""",
    """<Data Name ='DestinationDRA'>.+?CN=({dest_dc}[^\s,]+)""",
    """<Data Name ='SourceDRA'>.+?CN=({src_dc}[^\s,]+)"""
  ]


}
```