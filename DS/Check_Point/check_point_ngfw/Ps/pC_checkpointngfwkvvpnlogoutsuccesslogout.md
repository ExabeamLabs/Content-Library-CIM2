#### Parser Content
```Java
{
Name = "checkpoint-ngfw-kv-vpn-logout-success-logout"
Vendor = "Check Point"
Product = "Check Point NGFW"
TimeFormat = "epoch_sec"
Conditions = [
"""CheckPoint"""
"""product:"""
"""action:"Log Out""""
"""vpn_"""
]
Fields = [
"""\W({host}[\w\-.]+) CheckPoint"""
"""\Wtime:"({time}\d{10})"""
"""\Wdomain_name:"({domain}[^"]+?)\s*""""
"""\Wtermination_reason:"({failure_reason}[^"]+?)\s*""""
"""\Wsrc:"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Waction:"({action}[^"]+)"""
"""\Wuser:"({last_name}[^,]+),\s*({first_name}[\w\s]+\S)\s*\(({account}.+?)\)"""
"""\Wuser:"({first_name}[\w\s]+[^\s,])\s+({last_name}[^\s,]+)\s*\(({account}.+?)\)"""
"""\Wifdir:"({direction}[^"]+)"""
"""\suser_dn:"+({user_ou}[^"]+)"""
"""\W(user|src_user_name|dst_user_name):"+.+?\((({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))\)"""
"""\W(user|src_user_name|dst_user_name):"(?:[^_"\s]+_)?(-|({email_address}[^@"\s]+@[^@"\s]+)|((({domain}[^\s]+?)[\\]+)?({user}[\w\.\-]{1,40}\$?)))\s*""""
"""\Wduration:"({session_duration}\d+)""""
]
DupFields = [
"action->event_name"
]
ParserVersion = "v1.0.0"


}
```