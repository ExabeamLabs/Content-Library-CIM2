#### Parser Content
```Java
{
Name = "pan-cortex-mix-alert-trigger-success-xdr"
Vendor = "Palo Alto Networks"
Product = "Cortex XDR"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
Conditions = [
"""CEF:"""
"""|Palo Alto Networks|Cortex XDR|"""
"""tenantname="""
"""deviceFacility="""
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
"""CEF:[^|]+?\|([^\|]+\|){4}({alert_name}[^\|]+)"""
"""CEF:([^\|]+\|){6}({alert_severity}\d+)\|"""
"""\WexternalId=({alert_id}\d+)"""
"""\Wcat=({alert_type}[^\=]+?)\s+\w+="""
"""\Wcs2=\"?({process_command_line}[^\n]+?)\s*\"?\s+cs2Label="""
"""initiatorPath=(System|({process_path}[^=]+))\s+(\w+=|$)"""
"""\Wcs1=({process_name}[^\=]+)\s+"""
"""\Wsuser=\['(((NT AUTHORITY|TEST|({domain}[^\\\=]+))\\+)?(N\/A|LOCAL SERVICE|SYSTEM|Administrator|NETWORK SERVICE|({user}[\w\.\-]{1,40}\$?)))(',\s|'\]\s+\w+=)"""
"""\Wshost=(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[^\=]+?))\s+\w+="""
"""\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s"""
"""\Wspt=({src_port}\d+)"""
"""\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s"""
"""\Wdpt=({dest_port}\d+)"""
"""\Wact=({action}[^$]+?)\s*($|\")"""
"""\WfileHash=({hash_sha256}[A-Za-z0-9]+)\s"""
"""\WfilePath=(System|({file_path}({file_dir}[^=]+\\)?({file_name}[^\s]+?((\.({file_ext}[^\s\.]+))|))))\s+\w+="""
"""\Wrequest=({malware_url}[^\=]+)\s+\w+="""
"""\Wincident=({additional_info}[^\s]+)\s+\w+="""
]
DupFields = ["alert_name->alert_subject"]
ParserVersion = "v1.0.0"


}
```