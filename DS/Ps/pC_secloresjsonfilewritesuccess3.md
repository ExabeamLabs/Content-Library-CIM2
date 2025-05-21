#### Parser Content
```Java
{
Name = seclore-s-json-file-write-success-3
ExtractionType = json
Conditions = [
  """"machine_name""""
  """"activity":"""
  """"user_name":"""
  """"offline_access_right":"""
  """"activity":3"""
]
ParserVersion = "v1.0.0"

esector-file-activity.Fields}[
    """ファイル移動\\",\\"({file_path}({file_dir}.*?[\\\/]+)?({file_name}[^\\\/]+?(\.({file_ext}[^\\\.]+))?))\\"""",
    """({event_name}ファイル移動)"""
  
}
```