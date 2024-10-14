#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-file-success-4663-6"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyyMMddHHmmss"
Conditions = [
"""EventCode = 4663;"""
"""An attempt was made to access an object."""
]
Fields = [
"""Computer(Name)? = "+({host}[\w\-.]+)""""
"""({event_name}An attempt was made to access an object)"""
"""EventCode = ({event_code}\d+)"""
"""TimeGenerated = "({time}[\d]+)\.\d\d\d"""
"""Account Name:\s+(?:|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+Account Domain:\s+(?:|({domain}.+?))\s+Logon ID:"""
"""Process Name:\s+(?:|({process_path}({process_dir}(?:[^"]+)?[\\\/])?({process_name}[^\\\/]+?)))\s+Access Request"""
"""Logon ID:\s+({login_id}[^\s]+)\s+Object:"""
"""Security ID:\s+({user_sid}[^\s]+)\s"""
"""Accesses:\s+(?:|({access}.+?))\s+Access Mask:\s*({access_mask}\w+)?"""
"""Object Name:.*\\({src_file_name}(?:[^\\:]+(?=\.))({src_file_ext}\.[^\\:\s]+)?|[^\\:\s]+)\s+Handle ID:"""
"""Object Name:\s+(?:|({file_dir}.+?)\\(?:[^\\]+?))\s+Handle ID:"""
"""Object Type:\s+(?:|({file_type}.+?))\s+Object Name:"""
]
DupFields = [
"host->src_host"
]
ParserVersion = "v1.0.0"


}
```