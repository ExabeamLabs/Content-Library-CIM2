#### Parser Content
```Java
{
Name = "citrix-cgateway-str-endpoint-authentication-fail-failedlogin"
Vendor = "Citrix"
Product = "Citrix Gateway"
TimeFormat = "MM/dd/yyyy:HH:mm:ss z"
Conditions = [
"""Client_ip"""
"""Failure_reason"""
"""LOGIN_FAILED"""
]
Fields = [
"""({host}[\w\-.]+)\s+({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d \w+) [^\s]+"""
"""({host}[\w\-.]+)\s+({time}\d\d\d\d\/\d\d\/\d\d:\d\d:\d\d:\d\d \w+) [^\s]+"""
"""User\s+(({domain}[^\s\\]+?)\\+)?({user}[^\s]+)"""
"""Client_ip\s+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""Failure_reason\s*\"({failure_reason}[^\"]+)"""
"""Browser .*?({user_agent}[^\"]+)"""
]
ParserVersion = "v1.0.0"


}
```