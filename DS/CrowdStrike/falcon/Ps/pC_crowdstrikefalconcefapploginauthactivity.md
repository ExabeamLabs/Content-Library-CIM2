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
  """\Wduser=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^@]+?))?)\s*(\w+=|$)"""
  """\Woutcome=({result}.+?)\s*(\w+=|$)"""
  """({app}FalconHost)"""
]
ParserVersion = "v1.0.0"


}
```