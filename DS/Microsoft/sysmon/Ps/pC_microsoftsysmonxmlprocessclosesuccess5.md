#### Parser Content
```Java
{
Name = "microsoft-sysmon-xml-process-close-success-5"
  Vendor = "Microsoft"
  Product = "Sysmon"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions = [ """Microsoft-Windows-Sysmon""", """<Provider Name =""", """<EventID>5</EventID>""", """<TimeCreated SystemTime=""" ]
  Fields = [
    """<TimeCreated SystemTime=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{7}Z)('|")"""
	"""<Provider Name\\*=('|")Microsoft-Windows-Sysmon('|") Guid=('|")\{({process_guid}[^}]+?)\}"""
	"""<EventID>({event_code}\d+)</EventID>"""
	"""<Task>({task_name}[^<]+)<"""
	"""<Keywords>({result}[^<]+)</Keywords>"""
	"""<Execution ProcessID\\*=('|")({process_id}\d+)"""
	"""<Execution.*?ThreadID=('|")({thread_id}\d+)"""
	"""<Computer>({dest_host}({host}[\w\-.]+?))</Computer>"""
	"""<Data Name =('|")ProcessGuid('|")>\{({process_guid}[^\}<]+)\}<"""
	"""<Data Name =('|")ProcessId('|")>({process_id}[^<]+)<"""
	"""<Security UserID\\*=('|")({user_sid}S-[^"']+)('|")\s*/>""",
  """<Data Name\\*=('|")User('|")>((NT AUTHORITY|NT-AUTORITÄT|({domain}[^\\<]+?))\\)?(SYSTEM|(NETWORK|LOCAL) SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>""",
	"""<Data Name =('|")Image('|")>({process_path}(({process_dir}[^<]+?)[\\\/]+)?({process_name}[^\/\\<]+))<"""
	"""<Data Name =('|")User('|")>((NT AUTHORITY|({domain}[^<\\\s]+))\\)?(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))<"""
	"""<Level>({run_level}[^<]+)<"""
  ]
  ParserVersion = "v1.0.0"


}
```