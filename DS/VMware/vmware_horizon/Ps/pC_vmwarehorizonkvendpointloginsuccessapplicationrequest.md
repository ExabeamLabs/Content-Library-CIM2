#### Parser Content
```Java
{
Name = "vmware-horizon-kv-endpoint-login-success-applicationrequest"
Vendor = "VMware"
Product = "VMware Horizon"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """ View """
  """ Severity"""
  """ Module"""
  """EventType="""
]
Fields = [
  """\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)"""
  """({app}View)"""
  """EventType="*({event_name}[^"]+)"""
  """UserDisplayName ="*(({domain}[^\\"]+)\\+)?({user}[^\\"]+)""""
  """SessionType="*({operation}[^"]+)"""
  """UserSID="*({user_sid}[^"]+)"""
  """Module="*({resource}[^"]+)"""
  """ApplicationId="*({object}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```