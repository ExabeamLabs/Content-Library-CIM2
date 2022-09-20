#### Parser Content
```Java
{
Name = jsonar-sonarg-json-database-login-success-sonarw
Vendor = "jSONAR"
Product = "SonarG"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """ sonarw """
  """"$date":"""
  """"OS User":"""
  """"Database Name":"""
]
Fields = [
  """({host}[\w.\-]+) sonarw """
  """"\$date":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
  """"DB User Name":"(({db_domain}[^\\"]+)\\+)?(SYSTEM|({db_user}[^\\"]+))"""
  """"OS User":"(({domain}[^\\"]+)\\+)?(SYSTEM|({user}[^\\"]+))"""
  """"Server IP":"({dest_ip}[^"]+)"""
  """"Service Name":"({service_name}[^"]+)"""
  """"Server Host Name":"({dest_host}[^"]+)"""
  """"Client Host Name":"({src_host}[^"]+)"""
  """"Database Name":"({db_name}[^"]+)"""
  """Client IP":"({src_ip}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```