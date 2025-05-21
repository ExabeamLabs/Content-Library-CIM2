#### Parser Content
```Java
{
Name = "zeek-z-json-file-read-success-analyzers"
Conditions = [
""""analyzers""""
""" zeek_files """
""""fuid""""
]
ParserVersion = "v1.0.0"

esector-file-activity.Fields}[
    """ファイル移動\\",\\"({file_path}({file_dir}.*?[\\\/]+)?({file_name}[^\\\/]+?(\.({file_ext}[^\\\.]+))?))\\"""",
    """({event_name}ファイル移動)"""
  
}
```