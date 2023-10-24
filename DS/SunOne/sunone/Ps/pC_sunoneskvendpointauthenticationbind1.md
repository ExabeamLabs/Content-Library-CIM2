#### Parser Content
```Java
{
Name = "sunone-s-kv-endpoint-authentication-bind-1"
Vendor = "SunOne"
Product = "SunOne"
TimeFormat = "dd/MMM/yyyy:HH:mm:ss Z"
Conditions = [
"""ldap-access:"""
""" BIND """
]
Fields = [
"""({host}[\w\-\.]+)\s+ldap-access:"""
"""ldap-access:\s*\[({time}\d+\/\w+\/\d+:\d+:\d+:\d+ (\-|\+)\d+)"""
"""\Wuid=({user}[\w\.\-]{1,40}\$?)"""
"""\sconnection from\s+({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}):({src_port}\d+)\s+to\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\sBIND .*?\sRESULT err=({result}\d+)"""
]
ParserVersion = "v1.0.0"


}
```