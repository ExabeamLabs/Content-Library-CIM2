#### Parser Content
```Java
{
Name = "sybase-s-json-database-query-success-selecttable"
Conditions = [
"""object_name"""
""""event_desc""""
""""select table""""
""""database_name""""
""""extra_info""""
]
ParserVersion = "v1.0.0"

esector-file-activity.Fields}[
    """ファイル移動\\",\\"({file_path}({file_dir}.*?[\\\/]+)?({file_name}[^\\\/]+?(\.({file_ext}[^\\\.]+))?))\\"""",
    """({event_name}ファイル移動)"""
  
}
```