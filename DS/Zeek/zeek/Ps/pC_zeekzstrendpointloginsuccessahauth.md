#### Parser Content
```Java
{
Name = "zeek-z-str-endpoint-login-success-ahauth"
Vendor = "Zeek"
Product = "Zeek"
TimeFormat = "epoch_sec"
Conditions = [
""" udp """
""" AUTH    """
""" ah_auth:"""
]
Fields = [
"""({time}\d{10})\.\d+\t({host}\S+)\t"""
"""\tah_auth:[^\t]*?\(ip=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\)"""
"""\tah_auth:[^\t]*?\s+ip\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\tah_auth:[^\t]*?\(hostname=({dest_host}[^)]+)\)"""
"""\tah_auth:[^\t]*?\s+hostname\s+({dest_host}[^\s]+)"""
"""\tah_auth:[^\t]*?\(hostname=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\)"""
"""\tah_auth:[^\t]*?\s+hostname\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""\tah_auth:[^\t]*?\s+username\s+(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
]
ParserVersion = "v1.0.0"


}
```