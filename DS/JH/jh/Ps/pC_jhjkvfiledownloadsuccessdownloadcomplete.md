#### Parser Content
```Java
{
Name = "jh-j-kv-file-download-success-downloadcomplete"
Vendor = "JH"
Product = "JH"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""Download complete"""
"""download_time:"""
]
Fields = [
"""login:\s*"*({user}[\w\.\-]{1,40}\$?)"""
"""login:\s*"*({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
"""ordernum:\s*"*({order_num}\d+)"""
"""s_date:\s*"*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
"""flag:\s*"*({access}[^"]+)"""
"""ip_address:\s*"*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""contact_id:\s*"*({contact_id}(-)?\d+)"""
"""source:\s*"*({download_source}[^"]+)"""
]
DupFields = [
"access->operation"
]
ParserVersion = "v1.0.0"


}
```