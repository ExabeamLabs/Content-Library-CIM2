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
""""timestamp":({time}\d+)"""
""""user":"(({email_address}[^@"\s]+@[^@"\s]+)|(({domain}[^"@\\\/\s]+)[\\\/]+)?({user}[^"@\\\/\s]+))\""""
"""duser=({external_address}[^@<]+@?[^\s,>]+)"""
""""app":"({process_path}[^"]+)"""
""""type":"({alert_type}[^"]+)"""
""""category":"(n\/a|({alert_type}[^"]+))"""
""""url":"({malware_url}[^"]+)"""
"""CEF:([^\|]+\|){6}({alert_severity}[^\|]+)"""
""""severity":"({alert_severity}[^"]+)"""
""""md5":"({hash_md5}[^"]+)"""
""""policy":"({alert_name}[^"]+)"""
""""alert_name":"\s*({additional_info}[^"]+)""""
""""alert_type":"({alert_name}[^"]+)"""
"""dpriv=({alert_name}[^=]+)\s+\w+="""
""""file_path":"({malware_file_name}[^"]+)"""
""""object":"({object}[^"]+)"""
""""breach_id":"\s*({alert_id}[^"]+)""""
"""duser=({user}[^\s]+)"""
""""organization_unit":"({user_ou}[^"]+)""""
""""shared_with":"({shared_with_at}[^"]+)""""
""""site":"({site_at}[^"]+)""""
]
DupFields = [
"malware_url->url"
"malware_file_name->file_path_at"
]
ParserVersion = "v1.0.0"


}
```