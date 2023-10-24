#### Parser Content
```Java
{
Name = "vms-openvms-kv-endpoint-login-fail-loginfailure"
Vendor = "VMS Software"
Product = "OpenVMS"
TimeFormat = "dd-MMM-yyyy HH:mm:ss.SS"
Conditions = [
"""Auditable event:"""
"""Remote interactive login failure"""
"""Username:"""
]
Fields = [
"""failure\s+Event time:\s+({time}\d\d-\w+-\d\d\d\d\s+\d\d:\d\d:\d\d\.\d\d)"""
"""failure\s+[^"]+Username:\s+({user}[\w\.\-]{1,40}\$?)\s+(\w+|$)"""
"""({event_name}Remote interactive login failure)"""
"""failure\s+[^"]+PID:\s+({process_id}[\w]+)\s+(\w+|$)"""
"""failure\s+[^"]+Process name:\s+({process_name}[^\s]+)\s+(\w+|$)"""
"""failure\s+[^"]+Status:\s+({result}[^"]+?)\s*""""
"""failure\s+[^"]+Terminal name:\s+({additional_info}[^\s]+)\s+(\w+|$)"""
"""failure\s+[^"]+Host:\s+({host}[A-Fa-f\d\.:]+)\s+(\w+|$)"""
"""failure\s+[^"]+Host:\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s+(\w+|$)"""
"""failure\s+[^"]+Status:\s+[^"]+,\s+({failure_reason}[^"]+)\s*(\w+=|'|"|$)"""
]
DupFields = [
"event_name->operation"
]
ParserVersion = "v1.0.0"


}
```