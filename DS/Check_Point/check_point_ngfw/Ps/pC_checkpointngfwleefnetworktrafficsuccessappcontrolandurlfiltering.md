#### Parser Content
```Java
{
Name = checkpoint-ngfw-leef-network-traffic-success-appcontrolandurlfiltering
  ParserVersion = v1.0.0
  Conditions = [ """LEEF""", """|Application Control AND URL Filtering|""" ]

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
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
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
    """\WusrName =({full_name}.+?)\s*\(\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*\)""",
    """LEEF:([^\|]*\|){2}({product_name}[^\|]+)\|[^\|]*\|({action}[^\|]+)""",
    """\Wrule_action=({action}.+?)(\s+\w+=|\s*$)""",
    """\WdestinationDnsDomain=(?:|({url}.+?))(\s+\w+=|\s*$)""",
    """\Wappi_name=({web_domain}.+?)(\s+\w+=|\s*$)""",
    """\Wurl=({url}[^=]+?)\s*\w+=""",
    """\Wdescription=({additional_info}[^=]+?)\s*\w+="""
  
}
```