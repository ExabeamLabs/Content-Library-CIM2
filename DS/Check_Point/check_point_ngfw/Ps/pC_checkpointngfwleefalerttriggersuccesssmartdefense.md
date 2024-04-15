#### Parser Content
```Java
{
Name = "checkpoint-ngfw-leef-alert-trigger-success-smartdefense"
Vendor = "Check Point"
Product = "Check Point NGFW"
TimeFormat = "epoch_sec"
Conditions = [
"""LEEF"""
"""|Check Point|SmartDefense|"""
"""attack="""
]
Fields = [
"""\Worigin=({host}.+?)(\s+\w+:?=|\s*$)"""
"""\Worigin_sic_name=CN\\=({origin_sic_name}[^,\s]+),"""
"""\Wcat=({alert_type}.+?)(\s+\w+:?=|\s*$)"""
"""\WdevTime=({time}\d{10})"""
"""\WperformanceImpact=({performance_impact}\d+)"""
"""\Wsev=({alert_severity}\d+)"""
"""\Wattack=({alert_name}.+?)(\s+\w+:?=|\s*$)"""
"""\Wattack_info=({attack_info}.+?)(\s+\w+:?=|\s*$)"""
"""\Wreason=({additional_info}.+?)(\s+\w+:?=|\s*$)"""
"""\Wconfidence_level=({confidence_level}\d+)"""
"""\WsrcPort=({src_port}\d+)"""
"""\Wservice=({dest_port}\d+)"""
"""\Wprotection_id=({protection_id}.+?)(\s+\w+:?=|\s*$)"""
"""\Wprotection_type=({protection_type}.+?)(\s+\w+:?=|\s*$)"""
"""\Wifdir=({direction}.+?)(\s+\w+:?=|\s*$)"""
"""\Wsrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\Wproto=({protocol}.+?)(\s+\w+:?=|\s*$)"""
"""\Wrule=({rule_count}\d+)(\s+\w+:?=|\s*$)"""
"""\Wrule_name=({rule}.+?)(\s+\w+:?=|\s*$)"""
"""\Wrule_uid=\{({rule_id}.+?)\}"""
"""\Wloguid=\{({log_uid}.+?)\}"""
"""\Wsrc_machine_name=({src_host}[^@=]+?)(@({domain}.+?))?(\s+\w+:?=|\s*$)"""
"""\Wdst_machine_name=({dest_host}[^@=]+?)(@({domain}.+?))?(\s+\w+:?=|\s*$)"""
"""\Wdst_user_name=({full_name}.+?)\s*\(({user}.+?)\)"""
"""\Wsrc_user_name=({full_name}.+?)\s*\(({user}.+?)\)"""
"""\WusrName =({full_name}.+?)\s*\(({user}.+?)\)"""
"""LEEF:([^\|]*\|){2}({product_name}[^\|]+)"""
"""\Wsignature=({event_name}.+?)(\s+\w+:?=|\s*$)"""
"""\Wsmartdefense_profile=({smartdefense_profile}.+?)(\s+\w+:?=|\s*$)"""
"""\Wurl=({ips_url}.+?)(\s+\w+:?=|\s*$)"""
"""\Wresource_probing=({ips_desc}.+?)(\s+\w+:?=|\s*$)"""
]
DupFields = [
"event_name->protection_name"
]
ParserVersion = "v1.0.0"


}
```