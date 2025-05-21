#### Parser Content
```Java
{
Name = "vms-openvms-kv-file-delete-success-objectdeletion"
Conditions = [
"""Auditable event:"""
"""Object deletion"""
"""Username:"""
]
ParserVersion = "v1.0.0"

esector-file-activity.Fields}[
    """ファイル移動\\",\\"({file_path}({file_dir}.*?[\\\/]+)?({file_name}[^\\\/]+?(\.({file_ext}[^\\\.]+))?))\\"""",
    """({event_name}ファイル移動)"""
  
}
```