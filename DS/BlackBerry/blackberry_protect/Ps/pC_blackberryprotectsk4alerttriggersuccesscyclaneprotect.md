#### Parser Content
```Java
{
Name = "blackberry-protect-sk4-alert-trigger-success-cyclaneprotect"
Vendor = "BlackBerry"
Product = "BlackBerry Protect"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""destinationServiceName =CylanceProtect"""
"""externalID="""
]
Fields = [
"""\d+\s+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3}Z)\s+"""
"""\WexternalID=({src_host}[\w.\-]+)"""
"""\Woutcome=({action}[^\s]+)"""
"""\Wcat=(|({alert_type}.+?))(\s+\w+=|\s*$)"""
"""Security Alert Detected by.*?Category \[({alert_subject}[^\]\[,]+?)\]"""
"""Security Alert Detected by.*?Category \[({alert_type}[^\]\[,]+?)\]"""
"""Security Alert Detected by.*?SubCategory \[({category}[^\]\[,]+?)\]"""
"""\Wfname=(|({malware_url}.+?))(\s+\w+=|\s*$)"""
"""\Wfname=(|({process_path}({process_dir}(?:(\w+:)*([\\\/]+[^\\\/"]+?)+?)?[\\\/]+)({process_name}[^"\\\/]+?)))\s+(\w+=|$)"""
"""\Wproto=(|({file_name}.+?))(\s+\w+=|\s*$)"""
"""\Wmsg=(|({additional_info}.+?))(\s+\w+=|\s*$)"""
"""\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""cylance_score":({alert_severity}[^",]+)"""
"""\WdestinationServiceName =(|({device_name}.+?))(\s+\w+=|\s*$)"""
""""md5":"({hash_md5}[^"]+)"""
""""name":"({file_name}[^"]+)""""
""""sha256":"({file_hash}[^"]+)""""
""""file_size":\s*({bytes}\d+),"""
]
DupFields = [
"alert_type->alert_name"
"file_name->name_at"
"file_hash->hash_sha256_at"
"device_name->alert_source"
]
ParserVersion = "v1.0.0"


}
```