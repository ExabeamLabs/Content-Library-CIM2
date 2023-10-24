#### Parser Content
```Java
{
Name = "unix-unix-str-user-password-expire-success-account"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy MMM dd HH:mm:ss"
  Conditions = [
	"""pam_unix(crond:account)"""
	"""expired password for user"""
  ]
  Fields = [
	"""\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+"""
	"""pam_unix\(sudo:auth\):\s*({event_name}[^$]*?)\s*$"""
	"""expired password for user ({account}[^\(]+?) \(({failure_reason}[^\)]+?)\)"""
	]
	DupFields = [
	"account->user"
	]
	ParserVersion = "v1.0.0"


}
```