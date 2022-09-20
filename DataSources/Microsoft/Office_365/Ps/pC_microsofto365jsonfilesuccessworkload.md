#### Parser Content
```Java
{
Name = microsoft-o365-json-file-success-workload
  Vendor = Microsoft
  Product = Office 365
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """,Operation"""", """"Workload"""", """"SharePoint,""" ]
  Fields = [
    """"CreationTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """,ItemType":"({file_type}[^,]+)""",
    """,Operation":"({access}[^,]+)""",
    """,SourceRelativeUrl":"({file_dir}[^",]+)""",
    """,ClientIP":"({src_ip}[A-Fa-f.\d:]+)""",
    """,UserAgent":"({user_agent}[^,]+)""",
    """"SourceFileExtension":"({src_file_ext}[^,]+)""",
    """,SourceFileName":"({file_name}[^,]+)""",
    """"Workload":"({app}[^,]+)""",
    ]
    DupFields = [ "access->operation", "file_name->object" ]
	ParserVersion = v1.0.0


}
```