#### Parser Content
```Java
{
Name = "cisco-duo-json-app-login-fail-adminloginerror"
Vendor = "Cisco"
Product = "Duo Access"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSZ"
Conditions = [
  """"action": "admin_login_error""""
  """error\""""
  """"username": """
  """"description": """"
]
Fields = [
""""username":\s*"({full_name}[^"]+)"""
""""username":\s*"({first_name}\S+)\s+({last_name}[^\s"\\]+)"""
""""action":\s*"({operation}[^"]+)""""
""""object":\s*"({object}[^"]+)""""
""""email\\"+:\s*\\"+({email_address}[^"]+?)\\"+"""
""""ip_address\\"+:\s*\\"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\\"+"""
""""error\\"+:\s*\\"+({failure_reason}[^"]+?)\\"+"""
]
ParserVersion = "v1.0.0"


}
```