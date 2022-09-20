#### Parser Content
```Java
{
Name = lanscope-cat-kv-endpoint-login-success-loginuser
Vendor = "LanScope"
Product = "LanScope Cat"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """LanScopeCat - LogonUserOn/Off"""
  """Status="""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d)\s+({host}\S+)\s+LanScopeCat\s+\-"""
  """\sEvent="({operation}[^"]+)"""
  """\sAgent="({dest_host}[^"]+)"""
  """\sLogonUser="({user}[^"]+)"""
  """\sDomain="({domain}[^"]+)"""
  """\sStatus="({result}[^"]+)"""
  """\sIPAddress="({src_ip}[a-fA-F\d.:]+)"""
]
ParserVersion = "v1.0.0"


}
```