#### Parser Content
```Java
{
Name = "vmware-carbonblackedr-leef-alert-trigger-success-huntingapt28"
Vendor = "VMware"
Product = "Carbon Black EDR"
TimeFormat = "MMM dd yyyy HH:mm:ss.SSS z"
Conditions = [
"""LEEF:"""
"""|Carbon_Black|Protection|"""
"""fileName ="""
]
Fields = [
"""({host}[\w\-.]+)\s+LEEF:"""
"""\WdevTime=({time}\w+\s+\d+\s+\d\d\d\d\s+\d\d:\d\d:\d\d\.\d+ \w+)"""
"""\WreceivedTime=({received_time}\w+\s+\d+\s+\d\d\d\d\s+\d\d:\d\d:\d\d\.\d+ \w+)"""
"""\Wcat=(|({alert_type}.+?))\s+(\w+=|$)"""
"""\Wsev=(|({alert_severity}.+?))\s+(\w+=|$)"""
"""\WexternalId=(|({alert_id}.+?))\s+(\w+=|$)"""
"""\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\WsrcHostName =(({domain}[^\\\s]+)\\+)?({src_host}[\w\-.]+)"""
"""\WsrcProcess=(|({process_path}({process_dir}[^,]*?)(\\+({process_name}[^\\,]+?))?))\s+(\w+=|$)"""
"""\WusrName =(({domain}[^\\\s]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""\WfilePath=(|({file_path}(({file_dir}[^=]+[^\\])\\+)?({file_name}.+?)))\s+(\w+=|$)"""
"""\WfileName =(|({file_name}[^\/,]+?(\.({file_ext}[^\/,\.]+?))?))\s+(\w+=|$)"""
"""\WfileHash=(|({old_hash}.+?))\s+(\w+=|$)"""
"""\WdstHostName =({dest_host}[\w\-.]+)"""
"""\WruleName =(|({rule}.+?))\s+(\w+=|$)"""
"""\WinstallerFileName =(|({src_process_name}.+?))\s+(\w+=|$)"""
"""\Wpolicy=(|({policy_name}.+?))\s+(\w+=|$)"""
"""\|Carbon_Black\|Protection\|([^\|]*?\|){1}({alert_name}[^\|]+)\|"""
"""\|Carbon_Black\|Protection\|([^\|]*?\|){1}({access}[^\|]+)\|"""
"""\|Carbon_Black\|Protection\|([^\|]*?\|){1}({access}[^\|]+?)(\s*\([^|]+)?\|"""
]
DupFields = [
"old_hash->new_hash"
]
ParserVersion = "v1.0.0"


}
```