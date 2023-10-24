#### Parser Content
```Java
{
Name = "extremenetworks-zwlanm-str-endpoint-login-fail-loginfailed"
Vendor = "Extreme Networks"
Product = "Zebra WLAN Management"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """%"""
  """SYSTEM-3-LOGIN_FAIL:"""
  """Log-in failed"""
]
Fields = [
  """({time}\d{1,4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2})"""
  """\s+({host}[^\s]+)\s+({event_code}%\d*SYSTEM-3-LOGIN_FAIL):\s+Log-in ({result}failed) for user '({user}[\w\.\-]{1,40}\$?)'\s+from '({protocol}[^']+)\'"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```