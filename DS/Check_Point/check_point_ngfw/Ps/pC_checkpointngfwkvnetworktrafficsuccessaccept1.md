#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-network-traffic-success-accept-1
  Product = "Check Point NGFW"
  ParserVersion = v1.0.0
  Conditions = [ """product:""", """action:"Accept"""" ]

checkpoint-firewall-1 = {
  Vendor = Check Point
  TimeFormat = "epoch_sec"
  Fields = [
    """ time:"({time}\d{10})""",
    """\W({host}[\w\-.]+) CheckPoint""",
    """ src:"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wxlatesrc:"({src_translated_ip}[A-Fa-f:\d.]+)""",
    """ dst:"(0\.0\.0\.0|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
    """\Wdst:"({dest_translated_ip}[A-Fa-f:\d.]+)""",
    """ xlatedst:"(0\.0\.0\.0|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
    """\Wdst:"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """ xlatedst:"({dest_translated_ip}0\.0\.0\.0)""",
    """ service_id:"({app_protocol}[^"]+)""",
    """\Waction:"({action}[^"]+)""",
    """\Wrule:"({rule}[^"]+?)\s*"""",
    """ rule_name:"({rule}[^"]+?)\s*"""",
    """\Wapp_rule_name:"({rule}[^"]+?)\s*"""",
    """ s_port:"({src_port}\d+)""",
    """\Wxlatesport:"({src_translated_port}\d+)""",
    """\Wxlatedport:"({dest_translated_port}\d+)""",
    """ ifdir:"({direction}[^"]+)""",
    """ origin:"({origin_ip}[A-Fa-f:\d.]+)""",
    """ origin_?sic_?name:"CN=({origin_name}[^",]+)""",
    """product:"({product_name}[^"]+)""",
    #slow (15ms -> 8ms)"""\W__policy_id_tag:"({product_name}[^"\[\{]+).+?product:"Log Update"""",
    #slow (15ms -> 8ms)"""product:"Log Update".+?__policy_id_tag:"({product_name}[^"\[\{]+)""",
    """ service:"({dest_port}\d+)""",
    """ proto:"({protocol}[^"]+)""",
    """\Wpeer_gateway:"({src_translated_ip}[A-Fa-f:\d.]+)""",
    """ rule_uid:"\{?({rule_id}[^"\}]+)""",
    """\Wapp_rule_id:"\{({rule_id}[^"\}]+)""",
    """\Wsrc_machine_name:"({src_host}[^"]+?)\s*"""",
    """\Wsrc_machine_name:"({src_host}[^"@]+)@({domain}[^"]+)""",
    """\Wdst_machine_name:"({dest_host}[^"]+?)\s*"""",
    """\Wdst_machine_name:"({dest_host}[^"@]+)@({domain}[^"]+)""",
    """\Wuser:"({user}[^"\(\)@]+?)\s*"""",
    """\Wuser:"({email_address}[^\(\)"@]+@[^\(\)"@]+)\s*"""",
    """\Wsrc_user_name:"(({user}[^"\(\)@]+?)|({email_address}[^"@\(\)]+@[\(\)^"@]+))\s*"""",
    """\Wdst_user_name:"(({user}[^"\(\)@]+?)|({email_address}[^"@]+@[^"@]+))\s*"""",
    """\Wuser:"({last_name}[^,"]+),\s*({first_name}[\w\s]+\S)\s*\(({account}[^"]+?)\)""",
    """\Wuser:"({first_name}[\w\s]+[^\s,\(])\s+({last_name}[^\s,\(]+)\s*\(({account}[^"]+?)\)""",
    """\Wuser:"({last_name}[^,"\(]+),\s*({first_name}[\w\s]+\S)\s*\([^\)]+?\)[^"]+?\(({user}[^"@\)]+?)(@({domain}[^"\)]+?))?\)"""
    """\Wuser:"({first_name}[\w\s]+[^\s,\(])\s+({last_name}[^\s,\(]+)\s*\([^\)]+?\)[^"]+?\(({user}[^"@\)]+?)(@({domain}[^"\)]+?))?\)"""
    """\Wreceived_bytes:"({bytes_in}\d+)""",
    """\Wsent_bytes:"({bytes_out}\d+)""",
    """\Wifname:"({interface_name}[^"]+)""",
    """\W(user|src_user_name|dst_user_name):"(?:[^_"\s]+_)?({user}[^"\s]+?)\s*""""
  ]
  DupFields = [ "action->event_name" 
}
```