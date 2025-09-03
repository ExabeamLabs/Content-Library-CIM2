#### Parser Content
```Java
{
Name = "microsoft-evsystem-xml-endpoint-activity-success-5857"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Microsoft WMI Log"
  TimeFormat = [ """yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ""", """yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ""" ]
  Conditions = [ """Microsoft-Windows-WMI-Activity""", """<EventID>5857<""" ]  
  Fields = [ 
    """<TimeCreated(?:\s*|.*)SystemTime=["']({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d{7,9}Z)["']""", 
		"""<EventID>({event_code}\d+)<\/EventID>""", 
		"""<Computer>({host}[\w.-]+)<\/Computer>""", 
		"""<HostProcess>({parent_process_name}[^<]+)<\/HostProcess>""",
    """<ProviderPath>({process_path}({process_dir}[^"]*?[\\\/]+)?({process_name}[^"\\\/]+?))<""",
		"""<Provider Name =["']({provider_name}[^'"]+)["']""", 
		"""<EventRecordID>({event_id}[^<]+)<\/EventRecordID>""", 
		"""<Level>({run_level}[^<]+)<""" ,
    """<Keywords>({result}[^<]+)""",
    """Guid=('|")\{({process_guid}[^}]+?)\}"""
    """<Execution ProcessID\\*=('|")({process_id}\d+)"""
    """ThreadID(\\)?=('|")({thread_id}\d+)"""
    """<Channel>({channel}[^<]+)<\/Channel>"""
    """<Security UserID\\*=('|")({user_sid}[^'"]+)('|")"""
  ]


}
```