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
"""\Wtime(:|=)"({time}\d{10})"""
"""assigned_ip:+"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""origin:"({origin_ip}[A-Fa-f:\d.]+)""",
"""action:"({action}[^",;]+)"""
"""src:"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""user:+"+CN=(?:[^_]+_)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""om:+"+({event_name}[^",;]+)"""
"""cu_rule_category:"({rule_type}[^"]+)"""
"""cvpn_category:"({category}[^"]+)"""
"""event_name:"({event_name}[^"]+)"""
"""origin_?sic_?name:"CN=({origin_name}[^",]+)"""
"""user:"({full_name}[^,:\("]+)\s\((({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\)"""
]
ParserVersion = "v1.0.0"


}
```