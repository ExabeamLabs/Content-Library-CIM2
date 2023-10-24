#### Parser Content
```Java
{
Name = "microsoft-o365-mix-app-activity-success-securitycompliancecenter"
Vendor = "Microsoft"
Product = "Microsoft 365"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSS", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd HH:mm:ss.SSS"]
Conditions = [
  """SecurityComplianceCenter"""
  """Workload"""
  """Operation"""
]
Fields = [
  """"CreationTime":"({time}\d\d\d\d-\d\d-\d\d\s*\d\d:\d\d:\d\d\.\d\d\d)""""
  """CreationTime"*:\s*"*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """CreationTime"*:\s*"*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,7})?Z)"""
  """Operation"*:\s*"+({operation}[^"]+)"*"""
  """destinationServiceName =({app}[^=]+?)\s+\w+="""
  """Workload"*:\s*"*({app}[^"]+)"""
  """"ObjectId":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)",""""
  """"f3u\\?":\\?"({email_address}[^@"]+@[^",\.]+\.[^",]+?)\\?""""
  """trc\\*"+:\\*"+({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""
  """"app-user-displayname":"({full_name}[^"]+)""",
  """"user-email":"({email_address}[^",@]+@[^",\.]+\.[^",]+)"""
  """"ResultStatus":"({result}[^"]+)"""
  """"src-account-name":"({account}[^"]+)"""
  """"UserId":"(NOT-FOUND|(\w+\-){4}\w+|({email_address}[^@",]+@[^",]+)|({user}[\w\.\-]{1,40}\$?))""""
]
ParserVersion = "v1.0.0"


}
```