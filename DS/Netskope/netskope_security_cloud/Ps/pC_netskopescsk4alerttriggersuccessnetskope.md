#### Parser Content
```Java
{
Name = netskope-sc-sk4-alert-trigger-success-netskope
Vendor = "Netskope"
Product = "Netskope Security Cloud"
TimeFormat = "epoch_sec"
Conditions = [
"""destinationServiceName =Netskope"""
""""alert":"yes""""
]
Fields = [
""""_insertion_epoch_timestamp"+:({time}\d+)"""
""""timestamp":({time}\d{10})"""
""""user":"(({email_address}[^@"\s]+@[^@"\s]+)|(({domain}[^"@\\\/\s]+)[\\\/]+)?({user}[\w\.\-]{1,40}\$?))\""""
"""duser=({external_address}[^@<]+@?[^\s,>]+)"""
""""app":"({process_path}[^"]+)"""
""""type":"({alert_type}[^"]+)"""
""""category":"(n\/a|({alert_type}[^"]+))"""
""""url":"({malware_url}[^"]+)"""
"""CEF:([^\|]+\|){6}({alert_severity}[^\|]+)"""
""""severity":"({alert_severity}[^"]+)"""
""""md5":"({hash_md5}[^"]+)"""
""""policy":"({policy_name}[^"]+)"""
""""alert_name":"\s*({additional_info}[^"]+)""""
""""alert_type":"({alert_name}[^"]+)"""
"""dpriv=({alert_name}[^=]+)\s+\w+="""
""""file_path":"({malware_file_name}[^"]+)"""
""""object":"({object}({file_name}[^"]+?(\.({file_ext}\w+))?))""""
""""breach_id":"\s*({alert_id}[^"]+)""""
"""duser=({user}[\w\.\-]{1,40}\$?)"""
""""organization_unit":"({user_ou}[^"]+)""""
""""shared_with":"({shared_with_at}[^"]+)""""
""""site":"({site_at}[^"]+)""""
""""file_size":\s*({bytes}\d+)"""
"""msg=.*?\[({alert_source}[^\]]+)\]:"""
]
DupFields = [
"malware_url->url"
"malware_file_name->file_path_at"
]
ParserVersion = "v1.0.0"


}
```