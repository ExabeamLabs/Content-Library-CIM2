#### Parser Content
```Java
{
Name = "microsoft-o365-sk4-file-download-success-group"
Product = "Microsoft 365"
Conditions = [
""""activityType":"Group""""
""""activityOperationType":"Assign""""
""""targetResourceType":""""
"""act="""
]
ParserVersion = "v1.0.0"

cef-microsoft-app-activity.Fields}[
    """"SourceFileExtension":"({file_ext}({src_file_ext}[^"]+))"""",
    """"SourceRelativeUrl":"({src_file_dir}[^"]+)"""",
    """"SourceRelativeUrl":"({file_dir}[^"]+)"""",
    """"FileSizeBytes":({bytes}\d+)"""
    """"Platform":\s*"({os}[^"]+)""""
    """"ObjectId":"(Unknown|Not Available|({object}[^"]+?))\s*""""
  
}
```