#### Parser Content
```Java
{
Name = "entrust-ie-kv-endpoint-login-success-sucesssauth"
Vendor = "Entrust"
Product = "Entrust Identity Enterprise"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""] User """
""" successfully authenticated a challenge."""
""" Authentication Type: """
""" Remote Address: """
]
Fields = [
"""\[({time}\d{4}-\d\d-\d\d \d\d:\d\d:\d\d)(\]|,\]|,\d+\])"""
"""\] User (({email_address}[^\@\s]+@[^\s]+)|(({domain}[^\\\/]+)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s"""
"""Authentication Type: ({auth_method}[^,]+),"""
"""Application Name: ({app}[^,]+),"""
"""Remote Address: ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""({additional_info}Token Used: [^,]+)"""
]
ParserVersion = "v1.0.0"


}
```