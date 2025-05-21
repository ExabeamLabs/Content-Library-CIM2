#### Parser Content
```Java
{
Name = epic-siem-cef-app-activity-success-unsecure
Conditions = [
  """CEF:"""
  """|Epic|Security-SIEM|"""
  """|UNSECURE|"""
]
ParserVersion = "v1.0.0"

esector-file-activity.Fields}[
    """ファイル移動\\",\\"({file_path}({file_dir}.*?[\\\/]+)?({file_name}[^\\\/]+?(\.({file_ext}[^\\\.]+))?))\\"""",
    """({event_name}ファイル移動)"""
  
}
```