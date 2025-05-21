#### Parser Content
```Java
{
Name = "dell-emcisilon-str-file-write-success-rename"
Conditions = [
""" Isilon"""
"""|RENAME|SUCCESS|"""
]
ParserVersion = "v1.0.0"

esector-file-activity.Fields}[
    """ファイル移動\\",\\"({file_path}({file_dir}.*?[\\\/]+)?({file_name}[^\\\/]+?(\.({file_ext}[^\\\.]+))?))\\"""",
    """({event_name}ファイル移動)"""
  
}
```