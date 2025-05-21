#### Parser Content
```Java
{
Name = "f5-bigip-str-vpn-login-success-01490549"
Vendor = "F5"
Product = "F5 Access Policy Manager"
TimeFormat = ["yyyy-MM-dd HH:mm:ss","yyyy-MM-dd HH:mm:ss Z", "yyyy-MM-dd HH:mm:ss z","yyyy-MM-dd'T'HH:mm:ssZ"]
Conditions = [
""" 01490549:5:"""
]
Fields = [
"""\d\d:\d\d\s+({host}[\w\-.]+)\s([^\s]+\s)?[^\s]+\[\d+\]"""
"""(\s|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[+-]\d\d:\d\d)\s({host}[\w\-.]+)\s"""
"""\s+01490549:5:.*?({session_id}[^\s:]+): Assigned """
"""IPv4:\s+({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
"""\sClient IP:\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sAccess_Profile="({access_group}[^"]+)""""
]
DupFields = ["host->dest_host"]
ParserVersion = "v1.0.0"


}
```