#### Parser Content
```Java
{
Name = "apache-guacamole-str-app-login-fail-authservice"
Vendor = "Apache"
Product = "Apache Guacamole"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""auth.AuthenticationService -"""
"""] WARN """
"""Authentication attempt from """
"""failed"""
]
Fields = [
"""Authentication attempt from \[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\,\s({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\]"""
"""for user "+({user}[\w\.\-\!\#\^\~]{1,40}\$?)"+ failed"""
]
ParserVersion = "v1.0.0"


}
```