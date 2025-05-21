#### Parser Content
```Java
{
Name = "vmware-nsxatp-cef-alert-trigger-success-mcafee"
Vendor = "VMware"
Product = "Lastline"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|McAfee|"""
"""deviceExternalId=Lastline Manager"""
]
Fields = [
"""\srt=({time}\d{13})"""
"""\sshost=({src_host}.+?)(\s+\w+=|\"*\s*$)"""
"""\ssuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+\w+=|\"*\s*$)"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\|McAfee\|.*?\|.*?\|.*?\|({alert_name}.*?)\|"""
"""\scat=({alert_type}.+?)(\s+\w+=|\"*\s*$)"""
"""\snitroSubcategory=({alert_type}.+?)(\s+\w+=|\"*\s*$)"""
"""\snitroThreat_Category=({alert_type}.+?)(\s+\w+=|\"*\s*$)"""
"""\sproto=({protocol}.+?)(\s+\w+=|\"*\s*$)"""
"""\sdpt=({dest_port}\d+)"""
"""nitro({hash_type}SHA1)=({file_hash}[^\s]+?)(\s+\w+=|\"*\s*$)"""
"""\snitroUniqueId=({alert_id}\d+)(\s+\w+=|\"*\s*$)"""
"""\snitroDevice_URL=({additional_info}[^\s]+?)(\s+\w+=|\"*\s*$)"""
]
DupFields = [
"host->dest_host"
]

ParserVersion = "v1.0.0"


}
```