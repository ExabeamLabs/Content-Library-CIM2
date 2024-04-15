#### Parser Content
```Java
{
Name = "pan-magnifier-cef-alert-trigger-success-lightcyber"
Vendor = "Palo Alto Networks"
Product = "Prisma Cloud"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""|LightCyber|Magna|"""
]
Fields = [
"""start=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
"""\|LightCyber\|Magna\|[^|]+?\|[^|]+?\|({alert_name}[^|]+?)\|"""
"""\|LightCyber\|Magna\|[^|]+?\|[^|]+?\|[^|]+?\|({alert_severity}[^|]+?)\|"""
"""\sexternalId=({alert_id}\d+)"""
"""\sshost=(?: |({src_host}.+?))\s*\w+="""
"""\ssuser=(?: |({user}.+?))\s*\w+="""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\scs1=(?: |({alert_type}.+?))\s*\w+="""
"""\smsg=(?: |({additional_info}.+?))\s*\w+="""
"""\sfilePath=(?: |({malware_url}.+?))\s*\w+="""
"""\|LightCyber\|Magna\|[^|]+?\|[^|]+?\|({alert_type}[^|]+?)\|[^"]+?\s+cs2=({alert_name}[^=]+?)\s+fileHash="""
]
DupFields = [
"host->dest_host"
"malware_url->process_name"
]
ParserVersion = "v1.0.0"


}
```