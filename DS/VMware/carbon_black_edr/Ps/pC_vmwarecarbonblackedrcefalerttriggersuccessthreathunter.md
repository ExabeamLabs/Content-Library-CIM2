#### Parser Content
```Java
{
Name = "vmware-carbonblackedr-cef-alert-trigger-success-threathunter"
Vendor = "VMware"
Product = "Carbon Black EDR"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|Carbon Black|"""
"""|Enterprise EDR|"""
"""|Threat_Hunter|"""
"""|Process """
""" was detected by the report """
]
Fields = [
""" ahost=({host}[\w.-]+)\s"""
""" rt=({time}\d{13})"""
""" dvchost=({dest_host}[\w.-]+)\s"""
""" dvc=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s"""
""" duser=({user}[^\s]+)"""
"""\|Process ({process_name}[^\|]+) was detected by the report"""
""" was detected by the report "+({alert_name}[^\|"]+)"""
"""\|Threat_Hunter\|[^\|]+\|({alert_severity}[^\|]+)"""
"""({alert_type}Threat_Hunter)"""
""" cs4="+({alert_id}[^"]+)"""
"""\|({event_name}Process [^\|]+ was detected by the report[^\|]+)\|"""
""" cs3=({additional_info}[^\s]+)"""
]
ParserVersion = "v1.0.0"


}
```