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
"""\Wcat=(|({alert_name}({alert_type}.+?)))(\s+\w+=|\s*$)"""
"""Security Alert Detected by.*?Category \[({alert_subject}[^\]\[,]+?)\]"""
"""Security Alert Detected by.*?Category \[({alert_name}({alert_type}[^\]\[,]+?))\]"""
"""Security Alert Detected by.*?SubCategory \[({category}[^\]\[,]+?)\]"""
"""\Wfname=(|({malware_url}.+?))(\s+\w+=|\s*$)"""
"""\Wfname=(|({process_path}({process_dir}(?:(\w+:)*([\\\/]+[^\\\/"]+?)+?)?[\\\/]+)({process_name}[^"\\\/]+?)))\s+(\w+=|$)"""
"""\Wproto=(|({name_at}({file_name}.+?)))(\s+\w+=|\s*$)"""
"""\Wmsg=(|({additional_info}.+?))(\s+\w+=|\s*$)"""
"""\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""cylance_score":({alert_severity}[^",]+)"""
"""\WdestinationServiceName =(|({alert_source}({device_name}.+?)))(\s+\w+=|\s*$)"""
""""md5":"({hash_md5}[^"]+)"""
""""name":"({name_at}({file_name}[^"]+))""""
""""sha256":"({hash_sha256_at}({file_hash}[^"]+))""""
""""file_size":\s*({bytes}\d+),"""
]
ParserVersion = "v1.0.0"


}
```