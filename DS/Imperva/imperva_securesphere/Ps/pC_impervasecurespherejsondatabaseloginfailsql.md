#### Parser Content
```Java
{
Name = imperva-securesphere-json-database-login-fail-sql
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
  """"sql-unauthorized-os-user""""
]
Fields = [
  """:\d\d:\d\d\s+({host}[\w.-]+)\s"""
  """"create-time":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\w{3})"""
  """"description":\s*"({result_reason}[^"]+)"""
  """"user-name":\s*"({user}[^"]+)"""
  """"source-ip":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"source-port":\s*"({src_port}\d+)"""
  """"dest-ip":\s*"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
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