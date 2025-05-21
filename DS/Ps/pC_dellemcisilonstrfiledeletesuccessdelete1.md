#### Parser Content
```Java
{
Name = "dell-emcisilon-str-file-delete-success-delete-1"
Conditions = [
""" Isilon"""
"""|DELETE|SUCCESS|"""
]
ParserVersion = "v1.0.0"

esector-file-activity.Fields}[
    """ファイル移動\\",\\"({file_path}({file_dir}.*?[\\\/]+)?({file_name}[^\\\/]+?(\.({file_ext}[^\\\.]+))?))\\"""",
    """({event_name}ファイル移動)"""
  
}
```