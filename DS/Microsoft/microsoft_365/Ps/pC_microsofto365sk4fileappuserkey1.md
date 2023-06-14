#### Parser Content
```Java
{
Name = microsoft-o365-sk4-file-app-userkey-1
  ParserVersion = v1.0.0
  Conditions = [ """"Workload": """", """"UserKey": """", """"Operation": """", """"Location": """" ]

o365-file-app-activity = {
    Vendor = Microsoft
    Product = Microsoft 365
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Fields = [
      """"CreationTime":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """"Operation":\s*"({operation}[^"]+)""",
      """"UserId":\s*"({email_address}[^:@]+@({email_domain}[^",]+\.[^",]+))",""",
      """"Workload":\s*"({app}[^"]+)"""",
      """"ObjectId":\s*"({object}[^"]+)""",
      """"Id":\s*"({object_id}[^"]+)"""",
      """"UserKey":\s*"([^@]+@[^"]+|(({domain}[^\\]+)[\\]+({user}[^"]+))|(NOT-FOUND|([a-f\d]+\-){4}[a-f\d]+|({=user}[^"]+)))"""",
      """"RecordType":\s*({object_type}[^,]+),""",
      """"ClientIP":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """"SourceFileName":\s*"({src_file_name}[^"]+)"""",
      """"SourceRelativeUrl":\s*"({src_file_path}[^"]+)"""",
      """"SourceFileExtension":\s*"({src_file_ext}[^"]+)"""",
      """"UserAgent":\s*"({user_agent}[^"]+)""""

}
```