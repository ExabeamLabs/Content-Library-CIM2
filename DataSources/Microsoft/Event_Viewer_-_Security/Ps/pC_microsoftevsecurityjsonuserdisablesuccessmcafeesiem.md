#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-user-disable-success-mcafeesiem
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
  """McAfee_SIEM:"""
  """A user account was disabled."""
]
Fields = [
  """({event_name}A user account was disabled)"""
  """"src_ip":"({src_ip}[^"]+)"""
  """"dst_ip":"({dest_ip}[^"]+)"""
  """"id":\d*({event_code}4725)"""
  """"firsttime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""
  """"DomainID":"({domain}[^"]+)"""
  """"HostID":"({host}[^"]+)"""
  """"UserIDSrc":"({user}[^"]+)"""
  """"Security_ID":"({user_sid}[^"]+)"""
  """"Source_Logon_ID":"({login_id}[^"]+)"""
  """"UserIDDst":"({dest_user}[^"]+)"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```