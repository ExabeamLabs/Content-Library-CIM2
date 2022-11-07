#### Parser Content
```Java
{
Name = imperva-securesphere-json-database-login-fail-sqlfailedlogin
Vendor = "Imperva"
Product = "Imperva SecureSphere"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssz"
Conditions = [
  """"product":"""
  """"SecureSphere""""
  """"server-group-name":"""
  """"description":"""
  """"violation-type":"""
  """"sql""""
  """"sql-failed-login""""
]
Fields = [
  """:\d\d:\d\d\s+({host}[\w.-]+)\s"""
  """"create-time":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\w{3})"""
  """"description":\s*"({failure_reason}[^"]+)"""
  """"user-name":\s*"({user}[^"]+)"""
  """"source-ip":\s*"({src_ip}[a-fA-F\d.:]+)"""
  """"source-port":\s*"({src_port}\d+)"""
  """"dest-ip":\s*"({dest_ip}[a-fA-F\d.:]+)"""
  """"dest-port":\s*"({dest_port}\d+)"""
  """"protocol":\s*"({protocol}[^"]+)"""
  """"server-group-name":\s*"({server_group}[^"]+)"""
  """"service-name":\s*"({service_name}[^"]+)"""
]
DupFields = [
  "user->db_user"
]
ParserVersion = "v1.0.0"


}
```