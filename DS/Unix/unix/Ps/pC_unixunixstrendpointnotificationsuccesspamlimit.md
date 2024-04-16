#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-notification-success-pamlimit"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy MMM dd HH:mm:ss"
  Conditions = [
	"""(crond:session):""",
	"""pam_limits"""
  ]
  Fields = [
	"""\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s"""
	"""pam_sss\(crond:session\):\s*({event_name}[^$]*?)\s*$"""
  ]
  ParserVersion = "v1.0.0"


}
```