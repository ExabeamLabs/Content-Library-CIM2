#### Parser Content
```Java
{
Name = "checkpoint-ngfw-cef-endpoint-login-success-update"
Conditions = [
"""CEF:"""
"""|Check Point|Identity Awareness|"""
"""act=Update"""
"""auth_status=Successful Login"""
]
ParserVersion = "v1.0.0"

checkpoint-auth.Fields}[
  """originsicname:"CN=({origin_name}[^",]+)""",
  """ifdir:"({direction}[^"]+)"""
  ]

}

{
Vendor = "Check Point"
Product = "Check Point NGFW"
TimeFormat = "epoch"
Fields = [
"""\Wrt=({time}\d{13})"""
"""\Wact=(|({action}.+?))(\s+\w+=|\s*$)"""
"""\Wifname=(|({src_interface}.+?))(\s+\w+=|\s*$)"""
"""\Woriginsicname=(|({user_ou}.+?))(\s+\w+=|\s*$)"""
"""\Wproduct=(|({product_name}.+?))(\s+\w+=|\s*$)"""
"""\Wservice_id=(|({protocol}.+?))(\s+\w+=|\s*$)"""
"""\Wrule_name=(|({rule}.+?))(\s+\w+=|\s*$)"""
"""\Wconn_direction=(|({direction}.+?))(\s+\w+=|\s*$)"""
"""\Wapp=(|({protocol}.+?))(\s+\w+=|\s*$)"""
"""\Wcp_severity=(|({alert_severity}.+?))(\s+\w+=|\s*$)"""
"""\W(s|d)user=({last_name}[^\s]+)\s+({first_name}[^\s]+)\s+-\s+\(({department}[^)]+)\)\s+-\s+({company}[^\s]+)\s+\((({email_address}[^@\s]+@[^)]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""\W(s|d)user=((CheckPoint|({last_name}[^\s]+))\s+(Firewall|({first_name}[^\s]+))\s+)\((({email_address}[^\s@]+@[^\)]+)|checkpointfw|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""\Wshost=(|({src_host}[\w\-.]+?)(@({domain}[^\s@]+))?)(\s+\w+=|\s*$)"""
"""\Wsntdom=(|({domain}.+?))(\s+\w+=|\s*$)"""
"""\Wos_name=(|({os}.+?))(\s+\w+=|\s*$)"""
"""\WdestinationTranslatedAddress=(0\.0\.0\.0|({dest_translated_ip}[a-fA-F\d.:]+))"""
"""\WsourceTranslatedAddress=(0\.0\.0\.0|({src_translated_ip}[a-fA-F\d.:]+))"""
"""\Worigin=({origin_ip}[a-fA-F\d.:]+)"""
"""\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""dvc=({host}[a-fA-F\d.:]+)"""
"""ahost=({host}[^\s]+)"""
"""\Wspt=({src_port}\d+)"""
"""\Wdpt=({dest_port}\d+)"""
"""\Wserver_inbound_bytes=({bytes_in}\d+)"""
"""\Wserver_outbound_bytes=({bytes_out}\d+)"""
"""\Win=({bytes_in}\d+)"""
"""\Wout=({bytes_out}\d+)"""
"""categoryOutcome=(\/)?({result}.+?)\s\w+="""
]
Name = "checkpoint-ngfw-cef-endpoint-login-success-update"
Conditions = [
"""CEF:"""
"""|Check Point|Identity Awareness|"""
"""act=Update"""
"""auth_status=Successful Login"""
]
ParserVersion = "v1.0.0"
},

{
  Name = "checkpoint-ngfw-str-network-traffic-success-decrypt"
  ParserVersion = "v1.0.0"
  Vendor = "Check Point"
  Product = "Check Point NGFW"
  TimeFormat = "epoch_sec"
  Conditions = ["""CheckPoint""", """product:""", """action:"Decrypt""""]
  Fields = [
""" time:\"+({time}\d{10})"""
"""\W({host}[\w\-.]+) CheckPoint"""
""" src:\"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wxlatesrc:\"+({src_translated_ip}[A-Fa-f:\d.]+)"""
""" dst:\"+(0\.0\.0\.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""
"""\Wdst:\"+({dest_translated_ip}[A-Fa-f:\d.]+)"""
""" xlatedst:\"+(0\.0\.0\.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""
"""\Wdst:\"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
""" xlatedst:\"+({dest_translated_ip}0\.0\.0\.0)"""
""" service_id:\"+({app_protocol}[^\"]+)"""
"""\Waction:\"+({action}[^\"]+)"""
"""\Wrule:\"+({rule}[^\"]+?)\s*\""""
""" rule_name:\"+({rule}[^\"]+?)\s*\""""
"""\Wapp_rule_name:\"+({rule}[^\"]+?)\s*\""""
""" s_port:\"+({src_port}\d+)"""
"""\Wxlatesport:\"+({src_translated_port}\d+)"""
"""\Wxlatedport:\"+({dest_translated_port}\d+)"""
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
"""\Wuser:\"+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*\""""
"""\Waction:\"+({event_name}[^\"]+)"""
"""\Wuser:\"+({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\s*\""""
"""\Wsrc_user_name:\"+(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({email_address}[^\"@\(\)]+@[\(\)^\"@]+))\s*\""""
"""\Wdst_user_name:\"+(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({email_address}[^\"@]+@[^\"@]+))\s*\""""
"""\Wuser:\"+({last_name}[^,\"]+),\s*({first_name}[\w\s]+\S)\s*\(({account}[^\"]+?)\)"""
"""\Wuser:\"+({first_name}[\w\s]+[^\s,\(])\s+({last_name}[^\s,\(]+)\s*\(({account}[^\"]+?)\)"""
"""\Wuser:\"+({last_name}[^,\"\(]+),\s*({first_name}[\w\s]+\S)\s*\([^\)]+?\)[^\"]+?\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^\"\)]+?))?\)"""
"""\Wuser:\"+({first_name}[\w\s]+[^\s,\(])\s+({last_name}[^\s,\(]+)\s*\([^\)]+?\)[^\"]+?\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^\"\)]+?))?\)"""
"""\Wreceived_bytes:\"+({bytes_in}\d+)"""
"""\Wsent_bytes:\"+({bytes_out}\d+)"""
"""\Wifname:\"+({interface_name}[^\"]+)"""
"""\W(user|src_user_name|dst_user_name):"(?:[^_"\s]+_)?(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*"""",
"""resource:"({url}[^";,]+)"""",
""" dns_query:"({dns_query}[^"]+?)\s*""""
"""\W(user|src_user_name|dst_user_name):"({full_name}[^\"\(]+?)\s*\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  
}
```