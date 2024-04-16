#### Parser Content
```Java
{
Name = "cisco-ise-cef-endpoint-login-success-userloginsuccess"
Vendor = "Cisco"
Product = "Cisco ISE"
TimeFormat = "epoch"
Conditions = [
"""A SSH CLI user has successfully logged in"""
"""|Cisco|Cisco ISE|"""
"""CEF:"""
]
Fields = [
"""\Wrt=({time}\d{13})"""
"""dvchost=({host}[^\s]+)"""
"""({event_name}A SSH CLI user has successfully logged in)"""
"""Cisco ISE\|*({event_code}\d+)\|"""
"""destinationServiceName =({app}[^\s]+)"""
"""cat=({category}[^\s]+)\s"""
"""deviceSeverity=({severity}[^\s]+)"""
"""({result}Success)"""
"""ad.User=({user}[\w\.\-]{1,40}\$?)"""
"""suser=({user}[\w\.\-]{1,40}\$?)"""
]
ParserVersion = "v1.0.0"


}
```