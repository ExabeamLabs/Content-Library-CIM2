#### Parser Content
```Java
{
Name = "f5-bigip-mix-vpn-login-success-01490500"
Vendor = "F5"
Product = "F5 Access Policy Manager"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
ExtractionType = json
Conditions = [
"""01490500:5:"""
]
Fields = [
"""\d\d:\d\d\s+({host}[^\s]+)\s([^\s]+\s)?[^\s]+\[\d+\]"""
""""host":\{"name":"({host}[^"]+)"""
"""hostname="({host}[^"]+)"""
"""\s+01490500:5:.*?({session_id}[^\s:]+): New session"""
"""client IP ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sAccess_Profile="({access_group}[^"]+)""""
"""exa_regex=\d\d:\d\d\s+({host}[^\s]+)\s([^\s]+\s)?[^\s]+\[\d+\]"""
"""exa_json_path=$.host.name,exa_field_name=host"""
"""exa_regex=hostname="({host}[^"]+)"""
"""exa_json_path=$.message,exa_regex=\s+01490500:5:.*?({session_id}[^\s:]+): New session"""
"""exa_json_path=$.message,exa_regex=client IP ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""exa_json_path=$.message,exa_regex=\sUsername\s+'\s*(({domain}[^\\\s]+?)(\\+))?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*'"""
]
DupFields = ["host->dest_host"]
ParserVersion = "v1.0.0"


}
```