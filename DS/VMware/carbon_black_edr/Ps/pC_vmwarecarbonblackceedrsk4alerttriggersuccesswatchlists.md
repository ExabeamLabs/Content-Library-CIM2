#### Parser Content
```Java
{
Name = "vmware-carbonblackceedr-sk4-alert-trigger-success-watchlists"
Vendor = "VMware"
Product = "Carbon Black EDR"
TimeFormat = "epoch"
Conditions = [
""""processPath":"""
""""watchLists""""
""""responseSeverity""""
""""deviceName""""
]
Fields = [
""""eventTime"+:\s*({time}\d{13})"""
"""deviceName"+:\s*"+({dest_host}[^"]+)"""
""""email"+:\s*"+({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"+,"""
"""internalIpAddress"+:\s*"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""md5"+:\s*"+({hash_md5}[^"]+)"""
"""responseSeverity"+:\s*({alert_severity}\d+)"""
""""type"+:\s*"+({alert_type}[^"]+)"""
"""watchLists"+:[^\}\]]+?"+name":\s*"+({alert_name}[^"]+)"""
""""threatId"+:\s*"+({alert_id}[^"]+)"""
""""url"+:\s*"+({additional_info}[^"]+)"""
""""processPath"+\s*:\s*"+({process_path}({process_dir}([^"]+)?[\\\/])?({process_name}[^\\\/"]+))""""
"""iocId"+:\s*"+({ioc}[^"]+)"""
"""OS:\s*({os}[^\s]+)"""
]
ParserVersion = "v1.0.0"


}
```