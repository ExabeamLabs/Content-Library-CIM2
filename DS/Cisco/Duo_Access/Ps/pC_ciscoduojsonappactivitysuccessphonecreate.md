#### Parser Content
```Java
{
Name = cisco-duo-json-app-activity-success-phonecreate
Vendor = Cisco
Product = Duo Access
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSZ"
Conditions = [
  """"action": """"
  """"object": """
  """"username": """
  """"description": """"
]
Fields = [
  """"host":\s*"({host}[^"]+)""""
  """"action":\s*"({operation}[^"]+)""""
  """"object":\s*"({object}[^"]+)""""
  """"description":\s*"\{({additional_info}.+?)\}"""
  """"username":\s*"({full_name}[^"]+)"""
  """"username":\s*"({first_name}\S+)\s+({last_name}[^\s"\\]+)"""
  """"realname\\"+:\s*\\"+({full_name}.+?)\\"+(,\s+|$)"""
  """"realname\\"+:\s*\\"+({first_name}\S+)\s+({last_name}[^\s\\]+)"""
  """"uname\\"+:\s*\\"+({user}[^"]+?)\\"+"""
  """"email\\"+:\s*\\"+({email_address}[^"]+?)\\"+"""
  """"ip_address\\"+:\s*\\"+({src_ip}[^"]+?)\\"+"""
]
ParserVersion = "v1.0.0"


}
```