#### Parser Content
```Java
{
Name = "clearsense-cs-sk4-app-activity-success-clearsenseaudit"
Conditions = [
  """requestClientApplication=ClearSense Audit"""
]
ParserVersion = "v1.0.0"

esector-file-activity.Fields}[
    """ファイル移動\\",\\"({file_path}({file_dir}.*?[\\\/]+)?({file_name}[^\\\/]+?(\.({file_ext}[^\\\.]+))?))\\"""",
    """({event_name}ファイル移動)"""
  
}
```