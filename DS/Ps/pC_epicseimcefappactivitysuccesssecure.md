#### Parser Content
```Java
{
Name = epic-seim-cef-app-activity-success-secure
Conditions = [
  """CEF:"""
  """|Epic|Security-SIEM|"""
  """|SECURE|"""
]
ParserVersion = "v1.0.0"

esector-file-activity.Fields}[
    """ファイル移動\\",\\"({file_path}({file_dir}.*?[\\\/]+)?({file_name}[^\\\/]+?(\.({file_ext}[^\\\.]+))?))\\"""",
    """({event_name}ファイル移動)"""
  
}
```