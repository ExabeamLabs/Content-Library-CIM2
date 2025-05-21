#### Parser Content
```Java
{
Name = "gallagher-ac-csv-physical-location-access-success-cardexitgranted"
Conditions = [
  """gallagher"""
  """Card Exit Granted"""
]
ParserVersion = "v1.0.0"

esector-file-activity.Fields}[
    """ファイル移動\\",\\"({file_path}({file_dir}.*?[\\\/]+)?({file_name}[^\\\/]+?(\.({file_ext}[^\\\.]+))?))\\"""",
    """({event_name}ファイル移動)"""
  
}
```