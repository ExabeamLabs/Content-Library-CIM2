#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-app-notification-updatestatus
  ParserVersion = v1.0.0
  Conditions = [ """CheckPoint""", """product:"Application Control URL Filtering"""", """update_status:""" ]
  Fields = ${DLCheckpointParsersTemplates.checkpoint-firewall-2.Fields} [
    """\Wupdate_status:"({result}[^"]+)"""
  ]

checkpoint-firewall-2 = {
  Vendor = Check Point
  Product = Check Point NGFW
  TimeFormat = "epoch_sec"
  Fields = [
    """\Wtime(=|:)"({time}\d{10})""",
    """\W({host}[\w\-.]+) CheckPoint""",
    """\Wuser:"({last_name}[^,]+),\s*({first_name}[\w\s]+\S)\s*\(({account}.+?)\)""",
    """\Wuser:"({first_name}[\w\s]+[^\s,])\s+({last_name}[^\s,]+)\s*\(({account}.+?)\)""",
    """\W(src|client_ip)(=|:)"*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wxlatesrc:"({src_translated_ip}[A-Fa-f:\d.]+)""",
    """\Wdst:"({dest_translated_ip}[A-Fa-f:\d.]+).+?xlatedst:"(0\.0\.0\.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
    """\Wdst(=|:)"*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?.+?xlatedst:"({dest_translated_ip}0\.0\.0\.0)""",
    """\Wservice_id:"({app_protocol}[^"]+)""",
    """\Waction:"({action}[^"]+)""",
    """\Wrule:"({rule}[^"]+)""",
    """\Wrule_name:"({rule}[^"]+)""",
    """\Wapp_rule_name:"({rule}[^"]+)""",
    """\Ws_port(=|:)"*({src_port}\d+)""",
    """\Wxlatesport:"({src_translated_port}\d+)""",
    """\Wxlatedport:"({dest_translated_port}\d+)""",
    """\Worigin:"({origin_ip}[^"]+)""",
    """\Worigin(_)?sic(_)?name:"CN=({origin_name}[^",]+)""",
    """\Wproduct:"({product_name}[^"]+)""",
    """\Wservice:"({dest_port}\d+)""",
    """\Wproto(=|:)"*({protocol}[^"]+)""",
    """\Wpeer_gateway:"({src_translated_ip}[A-Fa-f:\d.]+)""",
    """\Wrule_uid:"\{?({rule_id}[^"\}]+)""",
    """\Wapp_rule_id:"\{({rule_id}[^"\}]+)""",
    """\Wsrc_machine_name:"({src_host}[^"]+?)\s*"""",
    """\Wsrc_machine_name:"({src_host}[^"@]+)@({domain}[^"]+)""",
    """\Wdst_machine_name:"({dest_host}[^"]+?)\s*"""",
    """\Wdst_machine_name:"({dest_host}[^"@]+)@({domain}[^"]+)""",
    """\W(user|src_user_name|dst_user_name):+"+CN=(?:[^_]+_)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """\Wactivity:"({operation}[^"]+)""",
    """status:"({result}[^"]+)""",
    """reason:"({failure_reason}[^"]+)""",
    """\Wdescription:"({additional_info}[^"]+)""",
    """\Wfile_size:"({bytes}\d+)"""
    """\W(user|src_user_name|dst_user_name):"({full_name}[^\"\(]+?)\s*\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
    """\Waction:"({event_name}[^"]+)""",
  
}
```