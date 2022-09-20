#### Parser Content
```Java
{
Name = microsoft-mysql-kv-database-login-success-14
Vendor = "Microsoft"
Product = "SQL Server"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
Conditions = [
  """HostName ="""
  """DatabaseName ="""
  """SessionLoginName ="""
  """EventClass="14""""
]
Fields = [
  """HostName ="+({host}[^"]+)"""
  """StartTime="+({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d.\d+)"""
  """DatabaseName ="+({db_name}[^"]+)"""
  """SessionLoginName ="+(({domain}[^\\"]+?)\\+({user}[^"]+)|({db_user}[^"]+))"""
  """NTDomainName ="+({domain}[^"]+)"""
  """TextData="+({db_query}.+?)\s*""""
  """EventClass="+({event_code}\d+)"""
  """ApplicationName ="+({app}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```