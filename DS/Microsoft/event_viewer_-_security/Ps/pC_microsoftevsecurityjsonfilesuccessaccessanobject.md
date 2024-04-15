#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-file-success-accessanobject"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""An attempt was made to access an object."""
"""computer_name"""
]
Fields = [
"""({event_name}An attempt was made to access an object)"""
""""(?:winlog\.)?computer_name\\*":\\*"({host}[^\\"]+)"""
"""@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""({event_code}4663)"""
"""Object(:|=).*?Object Type(:|=)\s*({file_type}.+?)[\s;]*Object Name(:|=)\s*({file_path}({file_dir}.*?)({file_name}[^\\\/;]+?(\.({file_ext}[^\.;\\]+?))?))[\s;]*Handle ID(:|=)"""
"""Process Name(:|=)\s*(?:|({process_path}.+?))[\s;]*Access Request Information(:|=)"""
"""Process Name(:|=).*\\({process_name}[^\\;]+?)[\s;]*Access Request Information(:|=)"""
"""Accesses(:|=)\s*({access}.+?)[\s;]*Access Mask(:|=)\s*({access_mask}\w+)"""
""""AccessList\\*":\\*"({access}[^"]+?)\s*""""
""""Account\\*":\\*"(({domain}[^\\\s"]+)\\+)?({user}[^\\\s"]+)"""
""""SubjectUserSid\\*":\\*"({user_sid}[^\s"]+)"""
""""SubjectLogonId\\*":\\*"({login_id}[^\s"]+)"""
""""ObjectName\\*":\\*"(-|({file_path}({file_dir}.*?)({file_name}[^\\\/;]+?(\.({file_ext}[^\.;]+?))?)))\s*""""
""""ObjectType":"(-|({file_type}[^\s"]+))"""
""""ProcessName":"(?: |({process_path}({process_dir}(?:[^";]+)?[\\\/])?({process_name}[^\\\/";]+?)))\s*""""
""""record_number"\s*:\s*\"({event_id}\d+)"""
""""SubjectUserName"\s*:\s*\"({user}[^\"]+)"""
""""SubjectDomainName"\s*:\s*\"({domain}[^\"]+)"""
""""ObjectName"\s*:\s*\"(?:({file_dir}[^\"]+?)\\+[^\"\\]+)""""
""""AccessList"\s*:\s*\"({access}.+?)""""
"""Access Request Information:[rnt\\]*Accesses:[rnt\\]*({access}.*)[rnt\\]*Access Mask:[rnt\\]*({access_mask}.+?)\s*(\"|$)"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```