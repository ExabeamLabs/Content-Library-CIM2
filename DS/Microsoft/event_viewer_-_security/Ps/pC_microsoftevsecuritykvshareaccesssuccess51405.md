#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-share-access-success-5140-5"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""A network share object was accessed"""
"""Account Name ="""
"""EventID=5140"""
]
Fields = [
"""({event_name}A network share object was accessed)"""
"""({event_code}5140)"""
"""ComputerName =({host}[^\s]+)"""
"""DetectTime=({time}\d\d\d\d-\d{1,2}-\d{1,2}\s\d{1,2}:\d{1,2}:\d{1,2})"""
"""Logon ID=\s*({login_id}\S+)"""
"""Account Name =\s*({user}[\w\.\-]{1,40}\$?)"""
"""Account Domain=\s*({domain}[^\s]+)"""
"""Object Type=\s*({file_type}[^\s]+)"""
"""Source Address=\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""({access}Read)"""
"""Share Name =\s*[\\\*]*({share_name}[^\s]+)\s*Share"""
"""Share Path=\s*[\\\?]*(\s*|({share_path}(({d_parent}.+?)\\)?(|({d_name}[^\\]+?)))\\?)\s*Access Request Information:"""
"""Source Port(=|:)\s*({src_port}\d+)"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```