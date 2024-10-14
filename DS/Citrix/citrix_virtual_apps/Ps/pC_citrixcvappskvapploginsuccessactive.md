#### Parser Content
```Java
{
Name = "citrix-cvapps-kv-app-login-success-active"
Vendor = "Citrix"
Product = "Citrix Virtual Apps"
TimeFormat = "MM/dd/yyyy HH:mm:ss zzz"
Conditions = [
"""FarmName ="""
"""XenApp"""
""" State="Active""""
]
Fields = [
"""ServerName =\"+({host}[^\"]+)\""""
"""CurrentTime=\"+({time}\d+/\d+/\d+ \d\d:\d\d:\d\d \w{3})"""
"""AccountName =\"+(({domain}[^\\]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""BrowserName =\"+({app}[^\"]+)"""
"""ClientName =\"+({src_host}[^\"]+)"""
"""ClientAddress=\"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""UserName =\"+({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
]
ParserVersion = "v1.0.0"


}
```