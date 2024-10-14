#### Parser Content
```Java
{
Name = "microsoft-exchange-kv-app-activity-softdelete"
Conditions = [
"""WORKLOAD=Exchange"""
"""COMMAND=SoftDelete"""
"""CLIENTPROCESSNAME="""
"""TS="""
]
ParserVersion = "v1.0.0"

cef-microsoft-app-activity.Fields}[
    """"SourceFileExtension":"({src_file_ext}[^"]+)"""",
    """"SourceRelativeUrl":"({src_file_path}[^"]+)"""",
    """"SourceRelativeUrl":"({file_path}({file_dir}([^"]+)?[\/\\])?[^"]+)""",
    """"FileSizeBytes":({bytes}\d+)"""
    """"Platform":\s*"({os}[^"]+)""""
    """"ObjectId":"(Unknown|Not Available|({object}[^"]+?))\s*""""
  ]
  DupFields = [ "src_file_path->src_file_dir","src_file_ext->file_ext" 
}
```