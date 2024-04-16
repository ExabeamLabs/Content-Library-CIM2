#### Parser Content
```Java
{
Name = "vmware-horizon-kv-endpoint-login-success-applicationrequest"
Vendor = "VMware"
Product = "VMware Horizon"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """ View """
  """ Severity"""
  """ Module"""
  """EventType="""
]
Fields = [
  """\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)"""
  """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\S+\s({host}[\w\-.]+)\s"""
  """({app}View)"""
  """EventType="*({event_name}[^"]+)"""
  """UserDisplayName ="(({domain}[^"\\]+)\\)?\\?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))""""
  """SessionType="*({operation}[^"]+)"""
  """UserSID="*({user_sid}[^"]+)"""
  """Module="*({resource}[^"]+)"""
  """ApplicationId="*({object}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```