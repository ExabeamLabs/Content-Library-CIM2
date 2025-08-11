#### Parser Content
```Java
{
Name = "microsoft-o365-sk4-file-write-success-filemodified"
ExtractionType = json
Product = "Microsoft 365"
Conditions= [ """"Operation":"FileModified"""", """"Workload":"""", """"SourceFileName":"""" ]
ParserVersion = "v1.0.0"

cef-microsoft-app-activity.Fields}[
    """"SourceFileExtension":"({src_file_ext}[^"]+)"""",
    """"SourceRelativeUrl":"({src_file_dir}[^"]+)"""",
    """"SourceRelativeUrl":"({file_dir}[^"]+)"""",
    """"FileSizeBytes":({bytes}\d+)"""
    """"Platform":\s*"({os}[^"]+)""""
    """"ObjectId":"(Unknown|Not Available|({object}[^"]+?))\s*""""
  ]
  DupFields = [ "src_file_name->file_name","src_file_ext->file_ext" 
}
```