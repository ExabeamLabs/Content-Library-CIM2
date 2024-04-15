#### Parser Content
```Java
{
Name = "amazon-awabastion-str-endpoint-login-success-logon"
Vendor = "Amazon"
Product = "AWS Bastion"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""bastion:"""
"""logging onto"""
]
Fields = [
"""\d\d:\d\d:\d\d\s+({host}[^\s]+)\s+bastion:"""
"""({event_name}logging onto)"""
"""bastion:({hostname}[^:]+):({user}[^:]+):\s"""
"""([^,]+,){2}\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```