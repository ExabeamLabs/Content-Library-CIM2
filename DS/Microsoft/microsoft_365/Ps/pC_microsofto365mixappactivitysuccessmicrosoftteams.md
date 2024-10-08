#### Parser Content
```Java
{
Name = "microsoft-o365-mix-app-activity-success-microsoftteams"
Vendor = "Microsoft"
Product = "Microsoft 365"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """Workload"""
  """"MicrosoftTeams""""
  """Operation"""
]
Fields = [
  """"CreationTime\\*"+:[\s\\]*"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """destinationServiceName =({app}[^=]+?)\s*deviceInboundInterface"""
  """Workload"*:\s*"*({app}[^"]+)"""
  """Workload"*:\s*"*({app}[^"]+)"*\}"""
  """ObjectId"*:\s*"*((?i)(Unknown)|({object}[^"]+))"*"""
  """Operation"*:\s*"*({operation}[^"]+)"*"""
  """UserKey"*:\s*"*({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"*"""
  """UserId"*:\s*"*({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"*"""
  """"ClientIP\\*"+:[\s\\]*"+\[?(::ffff:)?({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9]+:[A-Fa-f0-9:]+))"""",
  """src-account-name":"({account_name}[^"]+)"""
  """UserAgent","Value":"({user_agent}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```