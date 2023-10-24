#### Parser Content
```Java
{
Name = "egnyte-egnyte-sk4-app-login-fail-username"
Vendor = "Egnyte"
Product = "Egnyte"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""username"""
"""destinationServiceName =Egnyte"""
"""logout_time"""
""""event":"Failed Login""""
]
Fields = [
""""time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)Z""""
"""requestClientApplication=({app}[^=]+?)\s\w+="""
"""dproc=({dproc}[^=]+)\s\w+="""
"""ipAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""ip_address":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""destinationServiceName =({event_subtype}[^=]+)\s\w+="""
"""([^\|]*\|){5}({operation}[^\|]+)\|"""
""""username":"({full_name}[^\(]+)\s\(\s*({email_address}[^@]+@({email_domain}[^\s\)]+))\s*\)""""
""""event":"({event_name}[^"]+)""""
]
DupFields = [
"dproc->category"
]
ParserVersion = "v1.0.0"


}
```