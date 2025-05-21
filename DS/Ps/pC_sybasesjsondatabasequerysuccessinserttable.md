#### Parser Content
```Java
{
Name = "sybase-s-json-database-query-success-inserttable"
Conditions = [
"""object_name"""
""""event_desc""""
""""insert table""""
""""database_name""""
""""extra_info""""
]
ParserVersion = "v1.0.0"

esector-file-activity.Fields}[
    """ファイル移動\\",\\"({file_path}({file_dir}.*?[\\\/]+)?({file_name}[^\\\/]+?(\.({file_ext}[^\\\.]+))?))\\"""",
    """({event_name}ファイル移動)"""
  
}
```