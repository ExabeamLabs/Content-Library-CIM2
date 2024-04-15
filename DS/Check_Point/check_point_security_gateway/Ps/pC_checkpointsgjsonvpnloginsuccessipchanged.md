#### Parser Content
```Java
{
Name = "checkpoint-sg-json-vpn-login-success-ipchanged"
Vendor = "Check Point"
Product = "Check Point Security Gateway"
TimeFormat = "epoch_sec"
Conditions = [
"""cvpn_category:"Session""""
"""product:"Connectra""""
"""action:"IP Changed""""
]
Fields = [
"""time:"+({time}\d{10})"""
"""assigned_ip:+"+({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""origin:+"+({src_translated_ip}[A-Fa-f:\d.]+)"""
"""action:"+({action}[^",;]+)"""
"""ifdir:"+({direction}[^",;]+)"""
"""src:+"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""user:+"+CN=(?:[^_]+_)?({user}[^",\s=\]]+)"""
"""om:+"+({event_name}[^",;]+)"""
]
ParserVersion = "v1.0.0"


}
```