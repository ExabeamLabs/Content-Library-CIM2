#### Parser Content
```Java
{
Name = "blackberry-protect-sk4-alert-trigger-success-terminate"
Vendor = "BlackBerry"
Product = "BlackBerry Protect"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""Cylance Protect"""
"""MEMORY_VIOLATION"""
"""outcome=terminate"""
"""|security-threat-detected|"""
]
Fields = [
"""created":"({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d)"""
""""user_name":"({user}[\w\.\-]{1,40}\$?)""""
""""process_id":({process_id}\d+)"""
""""image_name":"({process_path}({process_dir}(\w:)?(?:[^:\]]+)?[\\\/])?({process_name}[^\\\/"\]]+?))""""
""""file_hash_id":"({hash_sha256}[^"]+)""""
""""groups":"({user_group_name}[^"]+)""""
""""device_id":"({device_id}[^"]+)""""
"""outcome=({action}terminate)"""
""" Category \[({alert_name}[^\]]+)\]"""
"""msg=({alert_type}[^:]+)"""
""""agent_event_id":"({alert_id}[^"]+)""""
""""file_hash_id":"({file_hash}[^"]+)""""
"""\sfname=([^=]*\\)?({file_name}[^\.]+\.({file_ext}[^\\:\s.]+)?)\s+\w+="""
"""msg.+?\[({alert_source}[^]]+)"""
"""\s*Category\s*\[({alert_type}[^\]]+)[^\|]*"""
]
DupFields = [
"file_hash->hash_sha256_at"
"file_name->name_at"
"alert_name"->"alert_subject"
]
ParserVersion = "v1.0.0"


}
```