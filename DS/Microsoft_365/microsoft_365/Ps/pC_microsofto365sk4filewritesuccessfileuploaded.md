#### Parser Content
```Java
{
Name = microsoft-o365-sk4-file-write-success-fileuploaded
Product = "Microsoft 365"
Conditions = [
  """"Operation":"FileUploaded""""
  """"Workload":""""
  """"SourceFileName":""""
]
ParserVersion = "v1.0.0"

cef-microsoft-app-activity.Fields}[
    """"ObjectId":"({file_path}({file_dir}[^"]+\/)({file_name}[^"]+?(\.({file_ext}[^"]+))?)?)"""",
    """"SourceFileExtension":"({src_file_ext}[^"]+)"""",
    """"SourceRelativeUrl":"({src_file_path}[^"]+)"""",
    """"SourceRelativeUrl":"({file_path}({file_dir}([^"]+)?[\/\\])?[^"]+)"""
		""""FileSizeBytes":({bytes}\d+)"""
  ]
  DupFields = [ "src_file_path->src_file_dir","src_file_ext->file_ext" 
}
```