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
"""\Wsrc:"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Waction:"({action}[^"]+)"""
"""\Wuser:"({last_name}[^,]+),\s*({first_name}[\w\s]+\S)\s*\(({account}.+?)\)"""
"""\Wuser:"({first_name}[\w\s]+[^\s,])\s+({last_name}[^\s,]+)\s*\(({account}.+?)\)"""
"""\Wifdir:"({direction}[^"]+)"""
"""\suser_dn:"+({user_ou}[^"]+)"""
"""\W(user|src_user_name|dst_user_name):"+.+?\(({user}[^)]+)\)"""
"""\W(user|src_user_name|dst_user_name):"(?:[^_"\s]+_)?({user}[^"\s]+?)\s*""""
]
DupFields = [
"action->event_name"
]
ParserVersion = "v1.0.0"


}
```