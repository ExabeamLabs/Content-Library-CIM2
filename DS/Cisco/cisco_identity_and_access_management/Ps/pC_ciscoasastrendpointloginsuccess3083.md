#### Parser Content
```Java
{
Name = "cisco-asa-str-endpoint-login-success-3083"
Vendor = "Cisco"
Product = "Cisco Identity and Access Management"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""%AAA-5-AAA_AUTH_ADMIN_USER"""
"""Authentication succeeded for admin user"""
"""aaa.c:3083"""
]
Fields = [
"""({additional_info}Authentication succeeded for admin user) '({user}[\w\.\-\!\#\^\~]{1,40}\$?)' on ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""%AAA-({priority}5)-({event_name}AAA_AUTH_ADMIN_USER)"""
"""aaa.c:({event_code}3083)"""
]
ParserVersion = "v1.0.0"


}
```