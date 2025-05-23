#### Parser Content
```Java
{
Name = "cisco-duo-json-app-login-fail-adminloginerror"
Vendor = "Cisco"
Product = "Cisco Identity and Access Management"
ExtractionType = json
TimeFormat = ["yyyy-MM-dd HH:mm:ss.SSSZ","epoch_sec"]
Conditions = [
  """"action":"""
  """"admin_login_error""""
  """error\""""
  """"username":"""
  """"description":"""
]
Fields = [
    """destinationServiceName =({app}\S+)"""
    """"timestamp"\s*:\s*({time}\d{10})""",
    """"event-name":"({event_name}[^"]+)"""",
    """"action":"({operation}[^"]+)"""",
    """"username":"(({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """"object":"({object}[^"]+)"""",
    """"error":\s*"({failure_reason}[^"]+)""",
    """"email\\"+:\s*\\"+({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\\""""
    """"ip_address"+:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """exa_json_path=$.timestamp,exa_regex=({time}\d{10})""",
"""exa_json_path=$.username,exa_field_name=full_name""",
"""exa_regex="username":\s*"({first_name}\S+)\s+({last_name}[^\s"\\]+)""",
"""exa_json_path=$.action,exa_field_name=operation""",
"""exa_json_path=$.object,exa_field_name=object""",
"""exa_regex="email\\"+:\s*\\"+({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\\""""
"""exa_regex=\\"ip_address\\"+:\s*\\"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\\""""
"""exa_regex="error\\"+:\s*\\"+({failure_reason}[^"]+?)\\""""
]
ParserVersion = "v1.0.0"


}
```