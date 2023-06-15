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
  """"ip_address\\"+:\s*\\"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\\"+"""
]
ParserVersion = "v1.0.0"


}
```