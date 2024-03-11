#### Parser Content
```Java
{
Name = microsoft-evsystem-xml-endpoint-stop-1074
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - System
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions = [ """<System><Provider""", """<EventID Qualifiers='""", """>1074</EventID>""", """<Computer>""", """Shutdown Type:""" ]
  Fields = [
    """<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)'/>""",
    """<Computer>({host}({dest_host}[\w\-]+)[^<]*)</Computer>""",
    """<Data Name ='param7'>(({domain}[^\\<]+?)\\)?({user}[^<]+)</Data>""",
    """({event_code}1074)</EventID>""",
    """<Message>The process [^<]+ has ({event_name}[^<]+?)\s+[\w\-]+\s+on behalf of user""",
# shutdown_type is removed
    """<Data Name ='param1'>({process_path}(({process_dir}[^\.]+)?\\)?({process_name}[^<\s]+)?)""",
    """<Data Name ='param3'>({failure_reason}[^<]+)</Data>""",
    """<Security UserID='({user_sid}[^<]+)'/>""",
# reason_code is removed
  ]


}
```