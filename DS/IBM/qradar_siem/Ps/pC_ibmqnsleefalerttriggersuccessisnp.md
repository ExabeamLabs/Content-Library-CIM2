#### Parser Content
```Java
{
Name = "ibm-qns-leef-alert-trigger-success-isnp"
Vendor = "IBM"
Product = "QRadar SIEM"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [
"""|IBM|ISNP|"""
"""|cat="""
]
Fields = [
"""(\||\W)SensorName =(.+?@\s*)?({host}[^\s]+)\s*(\w+=|$)"""
"""\W({host}[\w\-\.]+)\s*LEEF:"""
"""(\||\W)devTime=({time}\w{3} \d\d \d\d\d\d \d\d:\d\d:\d\d)"""
"""(\||\W)src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+"""
"""(\||\W)dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s+"""
"""(\||\W)srcPort=({src_port}\d+)\s+"""
"""(\||\W)dstPort=({dest_port}\d+)\s+"""
"""(\||\W)proto=({protocol}.+?)\s*(\w+=|$)"""
"""(.*?\|){4}({alert_name}[^\|]+?)\|"""
"""(\||\W)event-type=({alert_type}.+?)\s*(\w+=|$)"""
"""(\||\W)sev=({alert_severity}.*?)\s*(\w+=|$)"""
"""(\||\W)nvpdata=({additional_info}.+?)\s(\w+=|$)"""
]
ParserVersion = "v1.0.0"


}
```