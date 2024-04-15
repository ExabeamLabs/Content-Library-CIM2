#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-login-fail-failedpamweblogin"
Vendor = "Unix"
Product = "Unix"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""failed pam web login:"""
]
Fields = [
"""\s({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2})\S+\s+({host}[^\s]+)\s+({process_name}[^\s]+)\s+({process_id}\d+)\s"""
"""web login:\s({user}[^\s@]+)@({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""({result}failed)"""
]
ParserVersion = "v1.0.0"


}
```