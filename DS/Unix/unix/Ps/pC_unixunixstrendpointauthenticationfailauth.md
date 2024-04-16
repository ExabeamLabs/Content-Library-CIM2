#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-authentication-fail-auth"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
	"""pam_unix(sudo:auth)"""
	"""could not identify password for"""
  ]
  Fields = [
	"""\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+"""
	"""pam_unix\(sudo:auth\):\s*({event_name}[^$]*?)\s*$"""
  ]
  ParserVersion = "v1.0.0"


}
```