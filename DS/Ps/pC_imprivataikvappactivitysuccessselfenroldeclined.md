#### Parser Content
```Java
{
Name = imprivata-i-kv-app-activity-success-selfenroldeclined
Conditions = [
  """Event: Self-Enrollment Declined"""
]
ParserVersion = "v1.0.0"

esector-file-activity.Fields}[
    """ファイル移動\\",\\"({file_path}({file_dir}.*?[\\\/]+)?({file_name}[^\\\/]+?(\.({file_ext}[^\\\.]+))?))\\"""",
    """({event_name}ファイル移動)"""
  
}
```