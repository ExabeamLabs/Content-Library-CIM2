#### Parser Content
```Java
{
Name = microsoft-evadfs-kv-log-clear-success-1102
Vendor = "Microsoft"
Product = "Event Viewer - ADFS"
TimeFormat = ["MM/dd/yyyy hh:mm:ss a", "dd-MM-yyyy HH:mm:ss"]
ParserVersion = "v1.0.0"
Conditions = [
"""EventCode=1102"""
"""SourceName =AD FS Auditing"""
"""Keywords="""
"""Message=The Federation Service authorized a request to one of the REST endpoints"""
]
Fields = [
  """({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d (AM|PM|am|pm))""",
	"""({event_name}The Federation Service authorized a request to one of the REST endpoints)"""
	"""\WEventCode=({event_code}\d+)""",
	"""User=(NULL|NOT_TRANSLATED|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """ComputerName =({dest_host}({host}[\w\-.]+))"""
	"""\WSourceName =({service_name}.+?)(\s+\w+=|\s*$)""",
	"""RecordNumber=({event_id}\w+)\s*""",
	"""Message=({additional_info}[^:\.]+?)(:|\.)""",
	"""EventType=(|({event_category}[^\s]+))\s""",
	"""Client IP:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
]


}
```