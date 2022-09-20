#### Parser Content
```Java
{
Name = checkpoint-ngfw-leef-network-traffic-success-urlfiltering
  ParserVersion = v1.0.0
  Conditions = [ """LEEF""", """|Check Point|URL Filtering|""" ]

leef-checkpoint-firewall = {
  Vendor = Check Point
  Product = Check Point NGFW
  TimeFormat = "epoch_sec"
  Fields = [
    """\Worigin=({host}.+?)(\s+\w+:?=|\s*$)""",
    """\Worigin_sic_name=CN\\=({origin_sic_name}[^,\s]+),""",
    """\Wcat=({action}.+?)(\s+\w+:?=|\s*$)""",
    """\WdevTime=({time}\d+)""",
    """\WsrcPort=({src_port}\d+)""",
    """\WdstPort=({dest_port}\d+)""",
    """\Wservice=({dest_port}\d+)""",
    """\Wifdir=({direction}.+?)(\s+\w+:?=|\s*$)""",
    """\Wifname=({src_interface}.+?)(\s+\w+:?=|\s*$)""",
    """\Wsrc=({src_ip}[a-fA-F\d.:]+)""",
    """\Wdst=({dest_ip}[a-fA-F\d.:]+)""",
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
    """\Wdst_user_name=({full_name}.+?)\s*\(\s*({user}.+?)\s*\)""",
    """\Wsrc_user_name=({full_name}.+?)\s*\(\s*({user}.+?)\s*\)""",
    """\WusrName =({full_name}.+?)\s*\(\s*({user}.+?)\s*\)""",
    """LEEF:([^\|]*\|){2}({product_name}[^\|]+)\|[^\|]*\|({action}[^\|]+)""",
    """\Wrule_action=({action}.+?)(\s+\w+=|\s*$)""",
  
}
```