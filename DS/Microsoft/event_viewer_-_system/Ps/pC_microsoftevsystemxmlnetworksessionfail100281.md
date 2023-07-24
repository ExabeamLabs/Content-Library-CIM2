#### Parser Content
```Java
{
Name = microsoft-evsystem-xml-network-session-fail-10028-1
  ParserVersion = "v1.0.0"
  Vendor = Microsoft
  Product = Event Viewer - System
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """<Provider Name ='Microsoft-Windows-DistributedCOM'""", """<EventID Qualifiers='""", """>10028<""", """<Computer>""", """<Data Name ='param3'>""" ]
  Fields = [
    """<Computer>({host}[^<]+)</Computer>""",
	  """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<TimeCreated SystemTime\\*='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """>({event_code}\d+)</EventID>""",
    """<Data Name ='param1'>(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[^<]+))</Data>""",
    """<Security UserID='({user_sid}[^']+)'\/>""",
    """<Data Name ='param3'>({process_path}(({process_dir}[^<]*?)[\\\/]+)?({process_name}[^<\\\/]+))<\/Data>""",
    """<Message>({additional_info}[^<]+)</Message>""",
    """<Keyword>({result}[^<]+)</Keyword>""",
    """<Execution ProcessID='({process_id}\d+)' ThreadID='({thread_id}\d+)'\/>"""
  ]


}
```