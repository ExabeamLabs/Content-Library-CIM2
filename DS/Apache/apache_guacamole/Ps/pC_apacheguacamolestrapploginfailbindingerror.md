#### Parser Content
```Java
{
Name = "apache-guacamole-str-app-login-fail-bindingerror"
Vendor = "Apache"
Product = "Apache Guacamole"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""] ERROR """
""" - Binding with the LDAP server at """
""" failed: Too many failed logins."""
]
Fields = [
"""Binding with the LDAP server at\s"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
"""user\s"({user_ou}[^"]+)""""
"""uid=({user_id}[^,]+)"""
"""({result}failed):\s({failure_reason}Too many failed logins)"""
]
ParserVersion = "v1.0.0"


}
```