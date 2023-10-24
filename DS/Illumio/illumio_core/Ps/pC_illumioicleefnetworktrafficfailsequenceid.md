#### Parser Content
```Java
{
Name = "illumio-ic-leef-network-traffic-fail-sequenceid"
Vendor = "Illumio"
Product = "Illumio Core"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""LEEF"""
"""[meta sequenceId="""
"""|Illumio|"""
]
Fields = [
"""pid=({process_id}\d+)"""
"""\|({action}[^\|]+)\|cat=({category}.+?)\s*\w+="""
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""\s+({host}[^\s]+)\s+illumio_pce"""
"""proto=({protocol}.+?)\s+\w+="""
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+\w+="""
"""dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s+\w+="""
"""sev=({alert_severity}\d+)"""
"""dstPort=({dest_port}\d+)"""
"""dstHostname=({dest_host}.+?)\s+\w+="""
"""dstHref=({uri_path}.+?)\s+\w+="""
""""app"+:"+({app}[^",]+)""""
""""loc"+:"+({location}[^",]+)""""
]
ParserVersion = "v1.0.0"


}
```