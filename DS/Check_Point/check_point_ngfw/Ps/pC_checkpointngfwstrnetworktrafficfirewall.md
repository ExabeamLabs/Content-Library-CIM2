#### Parser Content
```Java
{
Name = "checkpoint-ngfw-str-network-traffic-firewall"
  ParserVersion = "v1.0.0"
  Conditions = ["""product=VPN-1 & FireWall-1""", """product:""", """action:""""]
  Vendor = "Check Point"
  Product = "Check Point NGFW"
  TimeFormat = "epoch_sec"
  Fields = [
"""\Wtime(:|=)"({time}\d{10})"""
"""\W({host}[\w\-.]+) CheckPoint"""
""" src:\"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wxlatesrc:\"+({src_translated_ip}[A-Fa-f:\d.]+)"""
""" dst:\"+(0\.0\.0\.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""
"""\Wdst:\"+({dest_translated_ip}[A-Fa-f:\d.]+)"""
""" xlatedst:\"+(0\.0\.0\.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""
"""\Wdst:\"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
""" xlatedst:\"+({dest_translated_ip}0\.0\.0\.0)"""
""" service_id:\"+({app_protocol}[^\"]+)"""
"""\Waction:\"+({action}[^\"]+)"""
"""\Wrule:\"+({rule}[^\"]+?)\s*\""""
""" rule_name:\"+({rule}[^\"]+?)\s*\""""
"""\Wapp_rule_name:\"+({rule}[^\"]+?)\s*\""""
""" s_port:\"+({src_port}\d+)"""
"""\Wxlatesport:\"+({src_translated_port}\d+)"""
"""\Wxlatedport:\"+({dest_translated_port}\d+)"""
""" ifdir:\"+({direction}[^\"]+)"""
""" origin:\"+({origin_ip}[A-Fa-f:\d.]+)"""
""" origin_?sic_?name:\"+CN=({origin_name}[^\",]+)"""
"""product:\"+({product_name}[^\"]+)"""
""" service:\"+({dest_port}\d+)"""
""" proto:\"+({protocol}[^\"]+)"""
"""\Wpeer_gateway:\"+({src_translated_ip}[A-Fa-f:\d.]+)"""
""" rule_uid:\"+\{?({rule_id}[^\"\}]+)"""
"""\Wapp_rule_id:\"+\{({rule_id}[^\"\}]+)"""
"""\Wsrc_machine_name:\"+({src_host}[^\"]+?)\s*\""""
"""\Wsrc_machine_name:\"+({src_host}[^\"@]+)@({domain}[^\"]+)"""
"""\Wdst_machine_name:\"+({dest_host}[^\"]+?)\s*\""""
"""\Wdst_machine_name:\"+({dest_host}[^\"@]+)@({domain}[^\"]+)"""
"""\Wuser:\"+({user}[\w\.\-]{1,40}\$?)\s*\""""
"""\Wuser:\"+({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\s*\""""
"""\Wsrc_user_name:\"+(({user}[\w\.\-]{1,40}\$?)|({email_address}[^\"@\(\)]+@[\(\)^\"@]+))\s*\""""
"""\Wdst_user_name:\"+(({user}[\w\.\-]{1,40}\$?)|({email_address}[^\"@]+@[^\"@]+))\s*\""""
"""\Wuser:\"+({last_name}[^,\"]+),\s*({first_name}[\w\s]+\S)\s*\(({account}[^\"]+?)\)"""
"""\Wuser:\"+({first_name}[\w\s]+[^\s,\(])\s+({last_name}[^\s,\(]+)\s*\(({account}[^\"]+?)\)"""
"""\Wuser:\"+({last_name}[^,\"\(]+),\s*({first_name}[\w\s]+\S)\s*\([^\)]+?\)[^\"]+?\(({user}[\w\.\-]{1,40}\$?)(@({domain}[^\"\)]+?))?\)"""
"""\Wuser:\"+({first_name}[\w\s]+[^\s,\(])\s+({last_name}[^\s,\(]+)\s*\([^\)]+?\)[^\"]+?\(({user}[\w\.\-]{1,40}\$?)(@({domain}[^\"\)]+?))?\)"""
"""\Wreceived_bytes:\"+({bytes_in}\d+)"""
"""\Wsent_bytes:\"+({bytes_out}\d+)"""
"""\Wifname:\"+({interface_name}[^\"]+)"""
"""\W(user|src_user_name|dst_user_name):\"+(?:[^_\"\s]+_)?(-|({email_address}[^@"\s]+@[^@"\s]+)|((({domain}[^\s]+?)[\\]+)?({user}[\w\.\-]{1,40}\$?)))\s*\""""
"""\Wuser:\"+({first_name}[\w\s]+[^\s,\(])\s+({last_name}[^\s,\(]+)\s*\(({user}[\w\.\-]{1,40}\$?)(\)|@)"""
"""\Waction:"({event_name}[^"]+)"""
"""message_info:"({event_name}[^"]+)""""
"""\Wattack_info:"({failure_reason}[^";]+)""",
"""resource:"({url}[^";,]+)""""
  ]
  DupFields = [
"action->result"
"bytes_out->bytes"
]


}
```