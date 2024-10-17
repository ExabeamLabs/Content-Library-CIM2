#### Parser Content
```Java
{
Name = "vmware-horizon-str-endpoint-login-fail-session"
Vendor = "VMware"
Product = "VMware Horizon"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """View The agent running on machine"""
  """has accepted an allocated session"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+\-]\d\d:\d\d)\s+({host}[\w\-.]+)\s+View The agent running on machine\s+({dest_host}[\w\-.]+)\s+has accepted an allocated session for user (({domain}[^\\\s]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+View"""
  """The agent running on machine\s+({dest_host}[\w\-.]+)\s+has accepted an allocated session"""
  """for user (?:({domain}[^\\\s]+)\\+)?(({email_address}[^@\\\s]+@[^@\\\s]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
]
ParserVersion = "v1.0.0"


}
```