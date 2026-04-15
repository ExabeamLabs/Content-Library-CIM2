#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-vpn-login-success-vpnrouting
  ParserVersion = v1.0.0
  Product = Check Point NGFW
  Conditions = [ """CheckPoint""", """action:"VPN Routing"""", """product:"VPN-1 & FireWall-1"""" ]

checkpoint-firewall-1 = {
  Vendor = Check Point
  TimeFormat = "epoch_sec"
  Fields = [
    """time(:|=)"({time}\d{10})""",
    """\W({host}[\w\-.]+) CheckPoint""",
    """ src:"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wxlatesrc:"({src_translated_ip}[A-Fa-f:\d.]+)""",
    """ dst:"(0\.0\.0\.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
    """\Wdst:"({dest_translated_ip}[A-Fa-f:\d.]+)""",
    """ xlatedst:"(0\.0\.0\.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
    """\Wdst:"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """ xlatedst:"({dest_translated_ip}0\.0\.0\.0)""",
    """ service_id:"({app_protocol}[^"]+)""",
    """\Waction:"({action}[^"]+)""",
    """\Wrule:"({rule}[^"]+?)\s*"""",
    """ rule_name:"({rule}[^"]+?)\s*"""",
    """\Wapp_rule_name:"({rule}[^"]+?)\s*"""",
    """ s_port:"({src_port}\d+)""",
    """\Wxlatesport:"({src_translated_port}\d+)""",
    """\Wxlatedport:"({dest_translated_port}\d+)""",
    """ conn_direction:"({direction}[^"]+)"""",
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
    """\Wsrc_machine_name:"({src_host}[^"@]+?)(@({src_domain}[^"]+))?"""",
    """\Wdst_machine_name:"({dest_host}[^"@]+?)(@({dest_domain}[^"]+))?"""",
    """\Wuser:"({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*"""",
    """\Wuser:"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\s*"""",
    """\Waction:"({event_name}[^"]+)""",
    """\Wsrc_user_name:"(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))\s*"""",
    """\Wdst_user_name:"(({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)|({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))\s*"""",
    """\Wuser:"({last_name}[^,"]+),\s*({first_name}[\w\s]+\S)\s*\(({account}[^"]+?)\)""",
    """\Wuser:"({first_name}[\w\s]+[^\s,\(])\s+({last_name}[^\s,\(]+)\s*\(({account}[^"]+?)\)""",
    """\Wuser:"({last_name}[^,"\(]+),\s*({first_name}[\w\s\-]+\S)\s*(\([^\)]+?\)[^"]+?)?\(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\)"""
    """\Wuser:"({first_name}[\w\s\-]+[^\s,\(])\s+({last_name}[^\s,\(]+)\s*(\([^\)]+?\)[^"]+?)?\(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\)"""
    """\W(received_bytes|client_inbound_bytes):"({bytes_in}\d+)""",
    """\W(sent_bytes|client_outbound_bytes):"({bytes_out}\d+)""",
    """\Wifname:"({interface_name}[^"]+)""",
    """\W(user|src_user_name|dst_user_name):"(?:[^_"\s]+_)?(-|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|((({domain}[^\s]+?)[\\]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s*""""
    """\Wapp_category:"({category}[^"]+)"""
    """\Wresource:"\s*({url}[^"]+)"""
    """\Wuser_agent:"\s*({user_agent}[^"]+)"""
    """\W(user|src_user_name|dst_user_name):"({full_name}[^\"\(]+?)\s*\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  checkpoint-firewall-1 = {
  Vendor = Check Point
  TimeFormat = "epoch_sec"
  Fields = [
    """time(:|=)"({time}\d{10})""",
    """\W({host}[\w\-.]+) CheckPoint""",
    """ src:"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wxlatesrc:"({src_translated_ip}[A-Fa-f:\d.]+)""",
    """ dst:"(0\.0\.0\.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
    """\Wdst:"({dest_translated_ip}[A-Fa-f:\d.]+)""",
    """ xlatedst:"(0\.0\.0\.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
    """\Wdst:"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """ xlatedst:"({dest_translated_ip}0\.0\.0\.0)""",
    """ service_id:"({app_protocol}[^"]+)""",
    """\Waction:"({action}[^"]+)""",
    """\Wrule:"({rule}[^"]+?)\s*"""",
    """ rule_name:"({rule}[^"]+?)\s*"""",
    """\Wapp_rule_name:"({rule}[^"]+?)\s*"""",
    """ s_port:"({src_port}\d+)""",
    """\Wxlatesport:"({src_translated_port}\d+)""",
    """\Wxlatedport:"({dest_translated_port}\d+)""",
    """ conn_direction:"({direction}[^"]+)"""",
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
    """\Wsrc_machine_name:"({src_host}[^"@]+?)(@({src_domain}[^"]+))?"""",
    """\Wdst_machine_name:"({dest_host}[^"@]+?)(@({dest_domain}[^"]+))?"""",
    """\Wuser:"({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*"""",
    """\Wuser:"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\s*"""",
    """\Waction:"({event_name}[^"]+)""",
    """\Wsrc_user_name:"(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))\s*"""",
    """\Wdst_user_name:"(({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)|({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))\s*"""",
    """\Wuser:"({last_name}[^,"]+),\s*({first_name}[\w\s]+\S)\s*\(({account}[^"]+?)\)""",
    """\Wuser:"({first_name}[\w\s]+[^\s,\(])\s+({last_name}[^\s,\(]+)\s*\(({account}[^"]+?)\)""",
    """\Wuser:"({last_name}[^,"\(]+),\s*({first_name}[\w\s\-]+\S)\s*(\([^\)]+?\)[^"]+?)?\(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\)"""
    """\Wuser:"({first_name}[\w\s\-]+[^\s,\(])\s+({last_name}[^\s,\(]+)\s*(\([^\)]+?\)[^"]+?)?\(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\)"""
    """\W(received_bytes|client_inbound_bytes):"({bytes_in}\d+)""",
    """\W(sent_bytes|client_outbound_bytes):"({bytes_out}\d+)""",
    """\Wifname:"({interface_name}[^"]+)""",
    """\W(user|src_user_name|dst_user_name):"(?:[^_"\s]+_)?(-|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|((({domain}[^\s]+?)[\\]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s*""""
    """\Wapp_category:"({category}[^"]+)"""
    """\Wresource:"\s*({url}[^"]+)"""
    """\Wuser_agent:"\s*({user_agent}[^"]+)"""
    """\W(user|src_user_name|dst_user_name):"({full_name}[^\"\(]+?)\s*\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  ]
}

cef-checkpoint-vpn-events = {
  Vendor = Check Point
  Product = Check Point Security Gateway
  TimeFormat = "epoch"
  Fields = [
    """\Wrt=({time}\d{13})""",
    """\Wdvc=({host}[A-Fa-f:\d.]+)""",
    """\Wdvchost=({host}[\w\-.]+)""",
    """\WAction:\s*({action}[^;]+)""",
    """\Wshost=({src_host}[\w\-.]+)""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wsuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """\WsourceGeoCountryCode=({src_country_code}\w+)"""
    """\WAction:\s*({event_name}[^;]+)""",
  ]
}

checkpoint-firewall-5 = {
  Vendor = Check Point
  TimeFormat = "dMMMyyyy HH:mm:ss"
  Fields = [
    """\Wtime="\s*({time}\d+\w+\d\d\d\d \d\d:\d\d:\d\d)""",
    """\Worig=({host}[^,]+)""",
    """\Waction=({action}[^,]+)""",
    """\Wrule=({rule}[^,]+)""",
    """\Wsrc=(?:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[^,]+))""",
    """\Ws_port=({src_port}\d+)""",
    """\Wdst=(?:({dest_ip}\d{1,3}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[^,]+))""",
    """\Wd_port=({dest_port}\d+)""",
    """\Wproto=({protocol}[^,]+)""",
    """\Wmessage_info="({alert_name}[^"]+)""",
    """\Wmessage_info="({alert_type}[^"]+)""",
  ]
}

checkpoint-firewall-4 = {
  Vendor = Check Point
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """<\d+>\w+ \d\d \d\d:\d\d:\d\d\S*?\s+({host}[\w.\-]+)""",
    """\WAction="({action}[^"]+)""",
    """\Wrule="({rule}[^"]+)""",
    """\Wrule_uid="({rule_uid}[^"]+)""",
    """\Wservice_id="({app_protocol}[^"]+)""",
    """\Wsrc="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wdst="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wproto="({protocol}[^"]+)""",
    """\Wpeer gateway="({src_translated_ip}[^"]+)""",
    """\Wservice="({dest_port}\d+)""",
    """\Ws_port="({src_port}\d+)""",
    """\Wsrc_machine_name="({src_host}[^"]+)""",
    """\Wsrc_machine_name="({src_host}[^"@]+)@({domain}[^"]+)""",
    """\Wdst_machine_name="({dest_host}[^"]+)""",
    """\Wdst_machine_name="({dest_host}[^"@]+)@({domain}[^"]+)""",
    """\W(user|dst_user_name)="({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """\W(user|dst_user_name)="({full_name}[^"\(]+?)\s*\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """\WAction="({event_name}[^"]+)""",
  ]
}

leef-checkpoint-firewall = {
  Vendor = Check Point
  Product = Check Point NGFW
  TimeFormat = "epoch_sec"
  Fields = [
    """\Worigin=({host}.+?)(\s+\w+:?=|\s*$)""",
    """\Worigin_sic_name=CN\\=({origin_sic_name}[^,\s]+),""",
    """\Wcat=({category}.+?)(\s+\w+:?=|\s*$)""",
    """\W(action|act)=({action}[^=]+?)\s*\w+="""
    """\WdevTime=({time}\d{10})""",
    """\WsrcPort=({src_port}\d+)""",
    """\WdstPort=({dest_port}\d+)""",
    """\Wservice=({dest_port}\d+)""",
    """\Wconn_direction=({direction}.+?)(\s+\w+:?=|\s*$)""",
    """\Wifname=({src_interface}.+?)(\s+\w+:?=|\s*$)""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Winzone=({inzone}.+?)(\s+\w+:?=|\s*$)""",
    """\Woutzone=({outzone}.+?)(\s+\w+:?=|\s*$)""",
    """\Wproto=({protocol}.+?)(\s+\w+:?=|\s*$)""",
    """\Wrule=({rule_count}\d+)(\s+\w+:?=|\s*$)""",
    """\Wrule_name=\s*({rule}.+?)(\s+\w+:?=|\s*$)""",
    """\Wrule_uid=({rule_id}.+?)(\s+\w+=|\s*$)""",
    """\Wrule_uid=\{({rule_id}.+?)\}""",
    """\Wloguid=\{({log_uid}.+?)\}""",
    """\Wservice_id=({service_id}.+?)(\s+\w+:?=|\s*$)""",
    """\Wpeer_gateway=({peer_gateway}.+?)(\s+\w+:?=|\s*$)""",
    """\Wsrc_machine_name=({src_host}[^@=]+?)(@({domain}.+?))?(\s+\w+:?=|\s*$)""",
    """\Wdst_machine_name=({dest_host}[^@=]+?)(@({domain}.+?))?(\s+\w+:?=|\s*$)""",
    """\Wdst_user_name=({full_name}.+?)\s*\(\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*\)""",
    """\Wsrc_user_name=({full_name}.+?)\s*\(\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*\)""",
    """\WusrName=({full_name}.+?)\s*\(\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*\)""",
    """LEEF:([^\|]*\|){2}({product_name}[^\|]+)\|[^\|]*\|({action}[^\|]+)""",
    """\Wrule_action=({action}.+?)(\s+\w+=|\s*$)""",
    """\WdestinationDnsDomain=(?:|({url}.+?))(\s+\w+=|\s*$)""",
    """\Wappi_name=({web_domain}.+?)(\s+\w+=|\s*$)""",
    """\Wurl=({url}[^=]+?)\s*\w+=""",
    """\Wdescription=({additional_info}[^=]+?)\s*\w+="""
  ]
}

s-checkpoint-firewall = {
  Vendor = Check Point
  Product = Check Point NGFW
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """"time=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """\|orig=({host}[^\|]+)\|""",
    """\|service=({app_protocol}[^\|]+)\|""",
    """\|action=({action}[^\|]+)\|""",
    """\|app_rule_name=({rule}[^\|]+)\|""",
    """\|src=(?:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[^\|]+))\|""",
    """\|s_port=({src_port}\d+)""",
    """\|dst=(?:({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[^\|]+))\|""",
    """\|proto=({protocol}[^\|]+)\|""",
    """\|src_machine_name=({src_host}[^\|]+)""",
    """\|src_user_name=[^(]+\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """\|user=[^(]+\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  ]
}

cef-checkpoint-firewall-1 = {
Vendor = Check Point
Product = Check Point NGFW
TimeFormat = "epoch_sec"
Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""
"""time:"({time}\d{10})""""
"""\W({host}[\w\-.]+) CheckPoint"""
"""loguid:"({log_uid}[^"]+)"""
"""origin:"({origin_ip}[^"]+)"""
"""product:"({product_name}[^"]+)"""
"""\Wdescription:"({additional_info}[^"]+)"""
"""version+:"({version}\d+)""""
"""status:(null|"({status_msg}[^"\s]+))"""
"""client_ip:"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
}
}

DLCheckpointParsersTemplates = {
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
  ]
},

checkpoint-firewall = {
  Vendor = Check Point
  Product = Check Point NGFW
  TimeFormat = "ddMMMyyyy HH:mm:ss"
  Fields = [
    """\WOriginip=(-|({host}.+?))(\s+[\w-]+=|"+\s*$)""",
    """\WOrigin=(-|({host}.+?))(\s+[\w-]+=|"+\s*$)""",
    """\"({time}[^"]+?)(\s+[\w-]+=|"+\s*$)""",
    """\WSIP=(-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)(\s+|\|)""",
    """\WDIP=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?(\s+|\|)""",
    """\WXlateSIP=({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(\s+|\|)""",
    """\WXlateDIP=({dest_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(\s+|\|)""",
    """\Wrule_name=(-|({rule}.+?))(\s+[\w-]+=|"+\s*$|\|)""",
    """\WUser=(-|({users}.+?))(\s+[\w-]+=|"+\s*$|\|)""",
    """\WSource=(-|({src_host}.+?))(\s+[\w-]+=|"+\s*$|\|)""",
    """\WSPort=(-|({src_port}\d+))(\s+[\w-]+=|"+\s*$|\|)""",
    """\WDPort=(-|({dest_port}\d+))(\s+[\w-]+=|"+\s*$|\|)""",
    """\WXlateSport=(-|({src_translated_port}\d+))(\s+[\w-]+=|"+\s*$|\|)""",
    """\WXlateDPort=(-|({dest_translated_port}\d+))(\s+[\w-]+=|"+\s*$|\|)""",
    """\WProtocol=(-|({protocol}.+?))(\s+[\w-]+=|"+\s*$|\|)""",
    """\WIFDirection=(-|({direction}.+?))(\s+[\w-]+=|"+\s*$|\|)""",
    """\WAction=(-|({action}.+?))(\s+[\w-]+=|"+\s*$|\|)""",
    """\WAction=(-|({email_subject}.+?))(\s+[\w-]+=|"+\s*$|\|)""",
  ]
},

checkpoint-firewall-3 = {
  Vendor = Check Point
  Product = Check Point NGFW
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """<\d+>\w+ \d\d \d\d:\d\d:\d\d\S*?\s+({host}[\w.\-]+)""",
    """\WAction="({action}[^"]+)""",
    """\Wrule="({rule}[^"]+)""",
    """\Wrule_uid="({rule_uid}[^"]+)""",
    """\Wservice_id="({app_protocol}[^"]+)""",
    """\Wsrc="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wdst="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wproto="({protocol}[^"]+)""",
    """\Wpeer gateway="({src_translated_ip}[^"]+)""",
    """\Wservice="({dest_port}\d+)""",
    """\Ws_port="({src_port}\d+)""",
    """\Wsrc_machine_name="({src_host}[^"]+)""",
    """\Wsrc_machine_name="({src_host}[^"@]+)@({domain}[^"]+)""",
    """\Wdst_machine_name="({dest_host}[^"]+)""",
    """\Wdst_machine_name="({dest_host}[^"@]+)@({domain}[^"]+)""",
    """\Wdst_user_name="({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*(\(|")""",
    """\Wuser="({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """\WAction="({event_name}[^"]+)""",
  ]
},

raw-checkpoint-firewall = {
  Vendor = Check Point
  TimeFormat = "epoch_sec"
  Fields = [
    """\s({host}[\w\-\.]+)\s+product:\s*VPN-1 & FireWall-1;""",
    """\s({action}\w+)\s+\S+\s+product:\s*VPN-1 & FireWall-1;""",
    """logger:\s*\d\d:\d\d:\d\d\s*({action}\w+)\s*({host}[\w.\-]+)""",
    """({product_name}VPN-1 & FireWall-1);""",
    """\s({event_name}\w+)\s+\S+\s+product:\s*VPN-1 & FireWall-1;""",
    """logger:\s*\d\d:\d\d:\d\d\s*({event_name}\w+)\s*({host}[\w.\-]+)""",
    """\Wdate=\s*({time}\d{10})[;\]]""",
    """\Wsrc:\s*(|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?);""",
    """\Ws_port:\s*(|({src_port}\d+));""",
    """\Wdst:\s*(|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?);""",
    """\Wservice:\s*(|({dest_port}\d+));""",
    """\Wproto:\s*(|({protocol}.+?));""",
    """\Wrule:\s*(|({rule}.+?));""",
    """\Wrule_name:\s*(|({rule}.+?));""",
    """\Wuser:\s*(|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^";]+));""",
    """\Wuser:\s*({full_name}.+?)\s*\(({account}.+?)\)""",
    """\Wsrc_machine_name:\s*({email_address}[^;]+@[^;]+?);""",
    """\Wpolicy_name=\s*(|({policy_name}.+?))[;\]]""",
    """\Wxlatesrc:\s*(|({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}));""",
    """\Wxlatesport:\s*(|({src_translated_port}\d+));""",
    """\Wxlatedst:\s*(|({dest_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}));""",
    """\Wxlatedport:\s*(|({dest_translated_port}\d+));""",
    """\Wservice_id:\s*(|({protocol}.+?));""",
  ]
},

}
  

#=================================================== Start of CheckpointParsers section ==================================================================  
CheckpointParsers = [

${CheckpointParsersTemplates.cef-checkpoint-firewall}{
  Name = checkpoint-ngfw-cef-vpn-login-success-authentication
  ParserVersion = v1.0.0
  Conditions = [ """CEF:""", """|Check Point|Identity Awareness|""", """act=Log In""", """VPN""", """auth_status=Successful Login""" ]
},
${CheckpointParsersTemplates.cef-checkpoint-firewall}{
  Name = checkpoint-ngfw-cef-vpn-login-success-login
  ParserVersion = v1.0.0
  Conditions = [ """CEF:""", """|Check Point|Connectra|""", """act=Log In""", """VPN""", """outcome=Success""" ]
},
${CheckpointParsersTemplates.cef-checkpoint-firewall}{
  Name = checkpoint-ngfw-cef-vpn-login-success-login-1
  ParserVersion = v1.0.0
  Conditions = [ """CEF:""", """|Check Point|Connectra|""", """act=Log In""", """vpn""", """outcome=Success""" ]
},
${CheckpointParsersTemplates.cef-checkpoint-firewall}{
  Name = checkpoint-ngfw-cef-vpn-logout-success-logout
  ParserVersion = v1.0.0
  Conditions = [ """CEF:""", """|Check Point|Identity Awareness|""", """act=Log Out""", """VPN""" ]
},

{
Name = "checkpoint-ngfw-kv-endpoint-login-fail-failed"
Conditions = [
  """CheckPoint"""
  """product:""""
  """action:"Failed Log In""""
]
ParserVersion = "v1.0.0"
Vendor = "Check Point"
Product = "Check Point NGFW"
TimeFormat = "epoch_sec"
Fields = [
  """\Wtime(:|=)"({time}\d{10})"""
  """\W({host}[\w\-.]+) CheckPoint"""
  """\Wuser:"(-|({email_address}[^@"\s]+@[^@"\s]+)|((({domain}[^\s]+?)[\\]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)))""""
  """\Wuser:"({last_name}[^,]+),\s*({first_name}[\w\s]+\S)\s*\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)\)"""
  """\Wuser:"({full_name}[^,:\("]+)\s\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)\)"""
  """\Wsrc:"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Wendpoint_ip:"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """host_ip:"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\Wauth_method:"({auth_method}[^"]+)"""
  """\Wauth_status:"({result}[^"]+)"""
  """\sstatus:"({result}[^"]+)"""
  """\WDomain:\s+({domain}[^";]+)"""
  """\Wdomain_name:"({domain}[^"]+)"""
  """\Worigin:"({origin_ip}[^"]+)"""
  """\Worigin_sic_name:"CN=({origin_name}[^",]+)"""
  """\Wproduct:"({product_name}[^"]+)"""
  """reason:"({failure_reason}[^"]+?)\s*""""
  """\Wsrc_machine_name:"({src_host}[\w\-.]+)"""
  """description:"({failure_reason}({additional_info}[^";]+))""""
  """\W(user|src_user_name|dst_user_name):"({full_name}[^\"\(]+?)\s*\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
]
},

${CheckpointParsersTemplates.cef-checkpoint-firewall}{
  Name = checkpoint-ngfw-cef-endpoint-login-success-identity
  ParserVersion = v1.0.0	
  Conditions = [ """CEF:""", """|Check Point|Identity Awareness|""", """act=Log In""" ]
},

${CheckpointParsersTemplates.checkpoint-auth}{
  Name = checkpoint-ngfw-cef-endpoint-login-success-identity-1
  ParserVersion = v1.0.0
  Conditions = [ """CheckPoint""", """product:"""", """action:"Update"""", """product:"Identity Awareness"""", """auth_status:"Successful Login"""" ]
  Fields = ${CheckpointParsersTemplates.checkpoint-auth.Fields}[
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
  ]
},

{
  Name = checkpoint-tm-kv-app-activity-success-threatemulation
  Vendor = Check Point 
  TimeFormat = "epoch_sec"
  Product = Check Point Threat Emulation
  ParserVersion = "v1.0.0"
  Conditions = [ """ CheckPoint """, """product:"Threat Emulation"""","""; originsicname:""","""action:"""" ]
  Fields = [
"""\Wtime(:|=)"({time}\d{10})"""
"""\W({host}[\w\-.]+) CheckPoint"""
""" src:\"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wxlatesrc:\"+({src_translated_ip}[A-Fa-f:\d.]+)"""
""" dst:\"+(0\.0\.0\.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""
"""\Wdst:\"+({dest_translated_ip}[A-Fa-f:\d.]+)"""
""" xlatedst:\"+(0\.0\.0\.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""
"""\Wdst:\"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
""" xlatedst:\"+({dest_translated_ip}0\.0\.0\.0)"""
""" service_id:\"+({app_protocol}[^\"]+)"""
"""\Waction:\"+({result}({action}[^\"]+))"""
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
"""\Wuser:\"+({user}[\w\.\-]{1,40}\$?)\s*\""""
"""\Wuser:\"+({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+.[^\]\s"\\,;\|]+))\s*\""""
"""\Wsrc_user_name:\"+({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+.[^\]\s"\\,;\|]+))\s*\""""
"""\Wdst_user_name:\"+({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+.[^\]\s"\\,;\|]+))\s*\""""
"""\Wuser:\"+({last_name}[^,\"]+),\s*({first_name}[\w\s]+\S)\s*\(({account}[^\"]+?)\)"""
"""\Wuser:\"+({first_name}[\w\s]+[^\s,\(])\s+({last_name}[^\s,\(]+)\s*\(({account}[^\"]+?)\)"""
"""\Wuser:\"+({last_name}[^,\"\(]+),\s*({first_name}[\w\s]+\S)\s*\([^\)]+?\)[^\"]+?\(({user}[\w\.\-]{1,40}\$?)(@({domain}[^\"\)]+?))?\)"""
"""\Wuser:\"+({first_name}[\w\s]+[^\s,\(])\s+({last_name}[^\s,\(]+)\s*\([^\)]+?\)[^\"]+?\(({user}[\w\.\-]{1,40}\$?)(@({domain}[^\"\)]+?))?\)"""
"""\Wreceived_bytes:\"+({bytes_in}\d+)"""
"""\Wsent_bytes:\"+({bytes_out}\d+)"""
"""\Wsent_bytes:\"+({bytes}\d+)"""
"""\Wifname:\"+({interface_name}[^\"]+)"""
"""\W(user|src_user_name|dst_user_name):\"+(?:[^_\"\s]+_)?(-|({email_address}[^@"\s]+@[^@"\s]+)|((({domain}[^\s]+?)[\\]+)?({user}[\w\.\-]{1,40}\$?)))\s*\""""
"""\Wuser:\"+({first_name}[\w\s]+[^\s,\(])\s+({last_name}[^\s,\(]+)\s*\(({user}[\w\.\-]{1,40}\$?)(\)|@)"""
"""\Waction:"({event_name}[^"]+)"""
"""message_info:"({event_name}[^"]+)""""
"""\Wattack_info:"({failure_reason}[^";]+)""",
"""resource:"({url}[^";,]+)""""
  """severity:"({alert_severity}[^"]+)""""
  """action_details:"({result}({action}[^"]+))"""
  """smartdefense_profile:"({smartdefense_profile}[^"]+)"""
  """confidence_level:"({confidence_level}[^"]+)"""
  """description:"({additional_info}[^"]+)"""
  """malware_action:"({malware_action}[^"]+)"""
  """malware_family:"({malware_family}[^"]+)"""
  """malware_rule_id:"\{({malware_id}[^"\}]+)\}"""
  """malware_rule_name:"({malware_name}[^"]+)"""
  """policy:"({policy_name}[^"]+)"""
  """protection_name:"({protection_name}[^"]+)"""
  """protection_type:"({protection_type}[^"]+)"""
  """resource:"({resource}[^";,]+)""""
  """layer_name:"({alert_name}[^"]+)"""
  """user_agent:"\s*({user_agent}[^"]+)"""
  """vendor_list:"({vendor_name}[^"]+)"""
  ]
}
}
```