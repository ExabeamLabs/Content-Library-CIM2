#### Parser Content
```Java
{
Name = "crowdstrike-falcon-cef-app-login-authactivity"
Vendor = "CrowdStrike"
Product = "Falcon"
TimeFormat = "epoch_sec"
Conditions = [
  """CEF:"""
  """|CrowdStrike|FalconHost|"""
  """cat=AuthActivityAuditEvent"""
]
Fields = [
  """\Wrt=({time}\d{10})"""
  """\Wduser=({user}[^=@]+?)(@({domain}[^@]+?))?\s*(\w+=|$)"""
  """\Woutcome=({result}.+?)\s*(\w+=|$)"""
  """({app}FalconHost)"""
]
DupFields = [
  "domain->email_domain"
]
ParserVersion = "v1.0.0"


}
```