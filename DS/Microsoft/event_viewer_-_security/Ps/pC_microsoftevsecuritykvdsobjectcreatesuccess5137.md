#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-ds-object-create-success-5137"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""A directory service object was created"""
"""Object:"""
"""Subject:"""
]
Fields = [
"""({event_name}A directory service object was created)"""
"""({event_code}5137)"""
"""ComputerName =({host}[^\s]+)"""
"""Account Name(:|=)\s*({user}[^\s]+)"""
"""Security ID(:|=)\s*({user_sid}[^\s]+)"""
"""Account Domain(:|=)\s*({domain}[^\s]+)"""
"""Logon ID(:|=)\s*({login_id}[^\s]+)"""
"""Directory Service:\s*Name(:|=)\s*({service_name}[^\s]+)\s*.*?Type(:|=)\s*({service_type}.*?Services)"""
"""GUID(:|=)\s*\{({guid}[^\}]+)"""
"""Operation:\s*Correlation ID(:|=)\s*\{({correlation_id}[^\}]+)"""
"""Object:\s*DN(:|=)\s*({object_dn}.+?)\s"""
"""Object:\s*.*?Class(:|=)\s*({ds_object_class}[^\s]+)"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```