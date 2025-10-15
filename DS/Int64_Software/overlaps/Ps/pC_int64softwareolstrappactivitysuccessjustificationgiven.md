#### Parser Content
```Java
{
Name = "int64software-ol-str-app-activity-success-justificationgiven"
	Vendor = "Int64 Software"
	Product = "OVERLAPS"
	TimeFormat = "dd/MM/yy HH:mm:ss.SSS"
	Conditions = [
			"""Justification given"""
			"""(User:"""
			]
	Fields = [
			"""({time}\d\d\/\d\d\/\d\d\s+\d\d:\d\d:\d\d.\d\d\d)"""
			"""\s+\[({severity}\w+)\s+\]\s+"""
			"""({event_name}Justification given)"""
			"""password of computer\s+({src_host}[\w\-\.]+)\:\s+({operation}[^\s+\(]+)\s+\("""
			"""\(User:\s+\[({user_id}\d+)\]\s+({domain}[^\/]+)\/({user}[\w\.\-\!\#\^\~]{1,40}\$?)\)"""
			]
	ParserVersion = "v1.0.0"


}
```