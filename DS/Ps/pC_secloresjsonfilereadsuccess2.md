#### Parser Content
```Java
{
Name = seclore-s-json-file-read-success-2
ExtractionType = json
Conditions = [
  """"machine_name""""
  """"activity":"""
  """"user_name":"""
  """"offline_access_right":"""
  """"activity":2"""
]
ParserVersion = "v1.0.0"

esector-file-activity.Fields}[
    """ファイル移動\\",\\"({file_path}({file_dir}.*?[\\\/]+)?({file_name}[^\\\/]+?(\.({file_ext}[^\\\.]+))?))\\"""",
    """({event_name}ファイル移動)"""
  
}
```