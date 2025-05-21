#### Parser Content
```Java
{
Name = "secureauth-login-kv-endpoint-login-success-20000"
Vendor = "SecureAuth"
Product = "SecureAuth Login"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""EventID="20000""""
"""Authentication Success"""
]
Fields = [
"""\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)\s"""
"""Timestamp="({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+Z)"""
"""\WUserHostAddress="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\WRealm="({realm}[^"]+)"""
"""\WAppliance="({host}[\w\-.]+)"""
"""\sHostName ="({host}[\w\-.]+)""""
"""\WAppliance="({dest_host}[\w\-.]+)"""
"""\WUserID="(({email_address}[^\@]+\@[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""\WPriority="({priority}\d+)"""
"""\WEventID="({event_code}\d+)"""
"""({event_name}Authentication Success)"""
"""UserAgent="({user_agent}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```