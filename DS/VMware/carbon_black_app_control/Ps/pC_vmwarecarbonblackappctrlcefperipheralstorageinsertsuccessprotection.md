#### Parser Content
```Java
{
Name = "vmware-carbonblackappctrl-cef-peripheral-storage-insert-success-protection"
Vendor = "VMware"
Product = "Carbon Black App Control"
TimeFormat = "epoch"
Conditions = [
"""|Carbon Black|Protection|"""
"""tached|"""
]
Fields = [
"""\srt=({time}\d{13})"""
"""\|Carbon Black\|Protection\|(.*?\|){2}({operation}[^\|]+)\|"""
"""(\||\s)dst=(|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)(\s+[\w-]+=|\s*$)"""
"""(\||\s)dhost=(|(\S+\\+)?({dest_host}.+?))\s+(\w+=|$)"""
"""(\||\s)dvc=(|({host_ip}.+?))\s+(\w+=|$)"""
"""(\||\s)dvchost=(|({host}.+?))(\s\w+=|\s*$)"""
"""(\||\s)msg=({operation_details}.+?)\.\s"""
"""(\||\s)msg=Device\s+'({device_id}.+?)'"""
"""(\||\s)msg=Device\s+'({device_id}[^']+?)\s*\([^']+'"""
]
ParserVersion = "v1.0.0"


}
```