#### Parser Content
```Java
{
Name = "vmware-view-kv-endpoint-login-success-agentconnected"
Vendor = "VMware"
Product = "VMware View"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """ View - """
  """AGENT_CONNECTED"""
]
Fields = [
  """\d\d:\d\d:\d\d\s+({host}[^\s]+)\s+\d+\s+"""
  """({app}View)"""
  """\s+({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)"""
  """\sUserSID="({user_sid}[^"]+)""""
  """UserDisplayName ="(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
  """MachineName ="({dest_host}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```