#### Parser Content
```Java
{
Name = microsoft-evsystem-xml-network-session-fail-10028
  ParserVersion = "v1.0.0"
  Vendor = Microsoft
  Product = Event Viewer - System
  TimeFormat = ["yyyy-MM-dd't'HH:mm:ss.SSSSSSSSS'z'", "yyyy-MM-dd'T'HH:mm:ss"]
  Conditions = [ """<provider name='microsoft-windows-distributedcom'""", """<eventid qualifiers='""", """>10028<""", """<computer>""" ]
  Fields = [
    """<computer>({host}[\w\-\.]+)<""",
	  """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<timecreated systemtime='({time}\d\d\d\d-\d\d-\d\dt\d\d:\d\d:\d\d\.\d{1,9}z)'/>""",
    """<TimeCreated SystemTime\\*='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """>({event_code}\d+)</eventid>""",
    """<data name='param1'>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?</data>""",
    """<security userid='({user_sid}[^']+)'\/>""",
    """<data name='param3'>({process_path}(({process_dir}[^<]*?)[\\\/]+)?({process_name}[^<\\\/]+))</data>""",
    """<message>({additional_info}[^<]+)</message>""",
    """<keyword>({result}[^<]+)</keyword>""",
    """<execution processid='({process_id}\d+)' threadid='({thread_id}\d+)'\/>"""
    """<Level>({run_level}[^<]+)<"""
  ]


}
```