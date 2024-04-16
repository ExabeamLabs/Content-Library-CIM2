#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-ds-object-activity-success-4662"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
"""CEF:0|"""
"""|Microsoft-Windows-Security-Auditing:4662|"""
"""An operation was performed on an object"""
]
Fields = [
"""({event_name}An operation was performed on an object)"""
"""({event_code}4662)"""
"""\srt=({time}\d{13})"""
"""ahost=({host}[^\s]+)"""
"""\sdhost=({dest_host}[\w\-.]+)"""
"""\sdntdom=(-|({domain}[^\s]+))"""
"""duser=(-|({user}[\w\.\-]{1,40}\$?))"""
"""\sduid=({login_id}[^\s]+)"""
"""agt=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""originalAgentAddress=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""amac=({src_mac}[^\s]+)"""
"""originalAgentMacAddress=({src_mac}[^\s]+)"""
"""cs5=({ds_object_type}[^=]+)\s\w+="""
"""fname=({ds_object_name}[^\s]+)"""
"""ad\.Object:Object_,?Server=({ds_object_class}[^=]+?)\s*([^=\s]+=|$)"""
"""ad\.Operation:Operation_,?Type=({operation}[^=]+?)\s*([^=\s]+=|$)"""
"""cs1=({access}[^=]+?)\s+\w+="""
]
DupFields = [ "ds_object_name->object" ]
ParserVersion = "v1.0.0"


}
```