#### Parser Content
```Java
{
Name = "asupim-a-cef-printer-activity-success-printcontrolevent"
Vendor = "ASUPIM"
Product = "ASUPIM"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""CEF:"""
"""Print Control Event"""
"""|ASUPIM|ASUPIM|"""
]
Fields = [
"""shost=({src_host}.+?)\s+\w+="""
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""({result}Allowed)"""
"""({event_name}Print Control Event)"""
"""({severity}Low)"""
"""suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+="""
"""suid=({suid}[^\s]+)\s+\w+="""
"""fname=({file_name}.+?)\s+\w+="""
"""fsize=({bytes}\d+)\s+\w+="""
"""cs1=({device_class}.+?)\s+\w+="""
"""cs2=({group_name}.+?)\s+\w+="""
"""cs6=({action}.+?)\s+\w+="""
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+\w+="""
"""smac=({src_mac}.+?)\s+\w+="""
"""cs3=({device_id}.+?)\s+\w+="""
"""cn1=({num_pages}\d+)\s+\w+="""
"""cn2=({num_pages}\d+)\s+\w+="""
"""dvchost=({host}.+?)\s+\w+="""
"""dvc=({host}.+?)\s+\w+="""
]
DupFields = [
"file_name->object"
]
ParserVersion = "v1.0.0"


}
```