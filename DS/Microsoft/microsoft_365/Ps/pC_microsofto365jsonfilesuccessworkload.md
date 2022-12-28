#### Parser Content
```Java
{
Name = microsoft-o365-json-file-success-workload
  Vendor = Microsoft
  Product = Microsoft 365
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """,Operation"""", """"Workload"""", """"SharePoint,""" ]
  Fields = [
    """"CreationTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """,ItemType":"({file_type}[^,]+)""",
    """,Operation":"({operation}[^,]+)""",
    """,SourceRelativeUrl":"({file_dir}[^",]+)""",
    """,ClientIP":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """,UserAgent":"({user_agent}[^,]+)""",
    """"SourceFileExtension":"({src_file_ext}[^,]+)""",
    """,SourceFileName":"({file_name}[^,]+)""",
    """"Workload":"({app}[^,]+)""",
    ]
    DupFields = [ "access->operation", "file_name->object" ]
	ParserVersion = v1.0.0


}
```