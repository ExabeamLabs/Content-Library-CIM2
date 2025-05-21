#### Parser Content
```Java
{
Name = "netwrix-auditor-xml-app-activity-success-1003"
Conditions = [
"""NetWrix"""
""">1003</EventID>"""
"""The following audit event was detected:"""
]
ParserVersion = "v1.0.0"

esector-file-activity.Fields}[
    """ファイル移動\\",\\"({file_path}({file_dir}.*?[\\\/]+)?({file_name}[^\\\/]+?(\.({file_ext}[^\\\.]+))?))\\"""",
    """({event_name}ファイル移動)"""
  
}
```