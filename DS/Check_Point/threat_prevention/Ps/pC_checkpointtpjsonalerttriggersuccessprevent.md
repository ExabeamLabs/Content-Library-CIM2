#### Parser Content
```Java
{
Name = "checkpoint-tp-json-alert-trigger-success-prevent"
Vendor = "Check Point"
Product = "Threat Prevention"
TimeFormat = "epoch_sec"
Conditions = [
"""CheckPoint"""
""""product:""""
"""action:"Prevent""""
]
Fields = [
"""\Wtime:"({time}\d{10})"""
"""\W({host}[\w\-.]+) CheckPoint"""
"""\Wsrc:"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wdst:"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\Waction:"({action}[^"]+)"""
"""\Wmalware_action:"({malware_action}[^"]+)"""
"""\Wmalware_family:"({malware_family}[^"]+)"""
"""\Ws_port:"({src_port}\d+)"""
"""\Wservice:"({dest_port}\d+)"""
"""\Wproto:"({protocol}[^"]+)"""
"""\Wconfidence_level:"({confidence_level}[A-Fa-f:\d.]+)"""
"""\Wifdir:"({direction}[^"]+)"""
"""\Wprotection_name:"({protection_name}[^"]+)"""
"""\Wprotection_type:"({protection_type}[^"]+)"""
"""\Wdestination_dns_hostname:"({destination_dns_hostname}[^"]+)"""
"""\Worigin:"({origin_ip}[^"]+)"""
"""\Worigin_sic_name:"CN=({origin_name}[^",]+)"""
"""\Wproduct:"({product_name}[^"]+)"""
"""\Wrule_uid:"\{({rule_id}[^"\}]+)"""
"""\Wseverity:"({alert_severity}[^"]+)"""
]
DupFields = [
"protection_name->alert_name"
"protection_type->alert_type"
]
ParserVersion = "v1.0.0"


}
```