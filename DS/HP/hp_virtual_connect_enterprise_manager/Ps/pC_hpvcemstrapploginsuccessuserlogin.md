#### Parser Content
```Java
{
Name = "hp-vcem-str-app-login-success-userlogin"
Vendor = "HP"
Product = "HP Virtual Connect Enterprise Manager"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""vcmd:"""
"""VCM user login :"""
]
Fields = [
"""\d\d:\d\d:\d\d\s({host}\S+)\svcmd:"""
"""VCM user login : ({auth_type}\w+)\s({domain}[^\\]+)\\({user}[^@]+)@({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""({event_name}user login)"""
"""({app}VCM)"""
]
ParserVersion = "v1.0.0"


}
```