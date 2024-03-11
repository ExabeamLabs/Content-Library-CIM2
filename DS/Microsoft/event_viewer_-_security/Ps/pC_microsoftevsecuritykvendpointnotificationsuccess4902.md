#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-notification-success-4902
	Vendor = Microsoft 
	Product = Event Viewer - Security
	TimeFormat = "dd-MM-yyyy HH:mm:ss"
	ParserVersion = "v1.0.0"
	Conditions = [
	"""EventCode=4902"""
	"""Microsoft Windows security auditing"""
	"""Policy ID:"""
	"""The Per-user audit policy table was created"""
	]
	Fields = [
		"""({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d (AM|PM|am|pm))""",
		"""\WEventCode=({event_code}\d+)""",
		"""ComputerName =({host}[\w\-.]+)""",
		"""Keywords=({result}.+?)(\s+\w+=|\s*$)""",
		"""RecordNumber=({event_id}\w+)\s*""",
		"""Message=({additional_info}[^:\.]+?)(:|\.)""",
		"""({event_name}A password was changed)""",
		"""EventType=(|({event_category}[^\s]+))\s""",
		"""Policy ID:\s*({policy_id}[^\s]+)"""
	]


}
```