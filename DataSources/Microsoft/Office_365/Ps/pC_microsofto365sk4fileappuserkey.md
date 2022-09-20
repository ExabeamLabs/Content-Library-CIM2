#### Parser Content
```Java
{
Name = microsoft-o365-sk4-file-app-userkey
Vendor = Microsoft
Product = Office 365
ParserVersion = v1.0.0
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [ """"Workload":"""", """"UserKey":"""", """"Operation":"""" ]
Fields = [
""""CreationTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
""""Operation":"({operation}[^"]+)""",
""""UserId":"({email_address}[^@]+@({email_domain}[^",]+))"""",
""""Workload":"({app}[^"]+)"""",
""""ObjectId":"({object}[^"]+)""",
""""Id":"({object_id}[^"]+)"""",
""""UserKey":"([^@]+@[^"]+|(({domain}[^\\]+)[\\]+({user}[^"]+))|(NOT-FOUND|([a-f\d]+\-){4}[a-f\d]+|({=user}[^"]+)))"""",
""""RecordType":({object_type}[^,]+),""",
""""ClientIP":"({src_ip}[^"]+)"""",
""""SourceFileName":"({src_file_name}[^"]+)"""",
""""SourceRelativeUrl":"({src_file_path}[^"]+)"""",
""""SourceFileExtension":"({src_file_ext}[^"]+)"""",
""""UserAgent":"({user_agent}[^"]+)""""
]


}
```