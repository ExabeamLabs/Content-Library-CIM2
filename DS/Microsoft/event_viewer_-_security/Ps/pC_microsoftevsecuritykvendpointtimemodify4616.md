#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-time-modify-4616
	ParserVersion = "v1.0.0"
	Vendor = Microsoft
	Product = Event Viewer - Security
	TimeFormat = ["MM/dd/yyyy hh:mm:ss a", "dd-MM-yyyy HH:mm:ss"]
	Conditions = [ 
  """Message=The system time was changed""", 
  """EventCode=4616""", 
  """Previous Time:""", 
  """New Time:"""  
  ]
	Fields = [
		"""({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s(?i)(AM|PM))""",
		"""\WEventCode=({event_code}\d+)""",
		"""ComputerName =({host}[\w\-.]+)""",
		"""Keywords=({result}.+?)(\s+\w+=|\s*$)""",
		"""RecordNumber=({event_id}\w+)\s*""",
		"""Message=({additional_info}[^:\.]+?)(:|\.)""",
		"""({event_name}The system time was changed)""",
		"""EventType=(|({event_category}[^\s]+))\s""",
		"""Security ID:\s*({user_sid}\S+)\s+Account Name:""",
		"""Account Name:\s*(LOCAL SERVICE|-|({user}[\w\.\-]{1,40}\$?))\s+Account Domain:""",
		"""Account Domain:\s*(NT AUTHORITY|-|({domain}\S+))\s+Logon ID:""",
		"""Logon ID:\s*({login_id}\S+)\s+""",
	]


}
```