#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-file-success-567-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""event_id":567,"""
"""Object Access Attempt:"""
]
Fields = [
"""({event_name}Object Access Attempt)"""
""""@timestamp"\s*:\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
""""(?:winlog\.)?computer_name"\s*:\s*"({host}[\w\-.]+?)""""
""""record_number"\s*:\s*"({event_id}\d+)"""
"""({event_code}567)"""
""""user"\s*:\s*\{[^\}]*"identifier"\s*:\s*"({user_sid}[^"]+)"""
""""user"\s*:\s*\{[^\}]*"name"\s*:\s*"({user}[\w\.\-]{1,40}\$?)"""
""""user"\s*:\s*\{[^\}]*"domain"\s*:\s*"({domain}[^"]+)"""
""""(param3|ObjectType)"\s*:\s*"({file_type}[^"]+)"""
""""(param5|ObjectName)"\s*:\s*"({file_path}[^"]+)"""
""""(param5|ObjectName)"\s*:\s*"([^"]*\\)?({file_name}[^\\\."]+(\.({file_ext}[^\.\\"]+))?)""""
""""(param5|ObjectName)"\s*:\s*"({file_dir}.+?)\\+[^\\]+""""
""""(param6|Accesses)"\s*:\s*"({access}.+?)""""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```