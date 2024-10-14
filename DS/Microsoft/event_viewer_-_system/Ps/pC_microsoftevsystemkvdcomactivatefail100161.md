#### Parser Content
```Java
{
Name = microsoft-evsystem-kv-dcom-activate-fail-10016-1
	Vendor = Microsoft 
	Product = Event Viewer - System
	TimeFormat = ["dd-MM-yyyy HH:mm:ss", "MM/dd/yyyy hh:mm:ss a"]
	ParserVersion = "v1.0.0"
	Conditions = [
	"""EventCode=10016"""
	"""for the COM Server application"""
	"""Keywords=Classic"""
	"""This security permission can be modified using the Component Services administrative tool"""
	]
	Fields = [
		"""({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s(?i)(AM|PM))""",
		"""\WEventCode=({event_code}\d+)""",
		"""ComputerName =({host}[\w\-.]+)""",
		"""\WSourceName =({service_name}.+?)(\s+\w+=|\s*$)""",
		"""RecordNumber=({event_id}\w+)\s*""",
		"""Message=({additional_info}[^:\.]+?)(:|\.)""",
		"""\WCLSID\s*\{({cls_id}[^}\s]+)\}\s*"""
		"""({failure_reason}The application-specific permission settings do not grant ({operation}.*) permission for the COM Server application)"""
		"""APPID\s+\{({app_id}[^\}]+)\}\s+"""
		"""User=(NULL|NOT_TRANSLATED|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
		"""user\s+({domain}[^\\]+)\\({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s"""
		"""\s+SID\s+\(({user_sid}[^\)]+)\)\s+from address\s+(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[^\s]+))\s"""
	]


}
```