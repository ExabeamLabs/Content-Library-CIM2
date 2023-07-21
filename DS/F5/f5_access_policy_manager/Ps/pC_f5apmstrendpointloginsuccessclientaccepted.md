#### Parser Content
```Java
{
Name = f5-apm-str-endpoint-login-success-clientaccepted
Vendor = "F5"
Product = "F5 Access Policy Manager"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
ParserVersion = v1.0.0
Conditions = [ """alert tmm""", """<CLIENT_ACCEPTED>""" ]
Fields = [
"""\d\d:\d\d:\d\d ({host}[^\s]+)"""
"""alert tmm\[({process_id}\d+)\]"""
"""IP:local_addr:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))[^:]*\s*port:\s*(({src_port}[\d]+))"""
"""IP:client:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))[^:]*(:({src_port}\d+))?"""
]


}
```