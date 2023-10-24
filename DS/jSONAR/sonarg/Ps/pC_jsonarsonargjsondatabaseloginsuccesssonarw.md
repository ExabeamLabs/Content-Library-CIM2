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
  """"OS User":"(({domain}[^\\"]+)\\+)?(SYSTEM|({user}[\w\.\-]{1,40}\$?))"""
  """"Server IP":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """"Service Name":"({service_name}[^"]+)"""
  """"Server Host Name":"({dest_host}[^"]+)"""
  """"Client Host Name":"({src_host}[^"]+)"""
  """"Database Name":"({db_name}[^"]+)"""
  """Client IP":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```