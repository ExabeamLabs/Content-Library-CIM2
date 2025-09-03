#### Parser Content
```Java
{
Name = "progress-sharefile-json-app-activity-eventid"
  Vendor = "Progress"
  Product = "Progress ShareFile"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  ExtractionType = json  
  Conditions = [ """destinationServiceName =Progress ShareFile""", """"Activity":""", """"Email":""", """"EventID":""", """"ItemName":""" ]
  Fields = [
    """exa_json_path=$.Date,exa_regex=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """exa_json_path=$.Email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """exa_json_path=$.IPAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.EventID,exa_field_name=event_code""",
    """exa_json_path=$.Location,exa_regex=(-|({country_code}[^,]+)),""",
    """exa_json_path=$.User,exa_field_name=full_name""",
    """exa_json_path=$.Activity,exa_field_name=operation""",
    """exa_regex="ItemName":\s*"({file_path}({file_dir}[^"]*[\/]+)\s*({file_name}[^\/"]+(\.({file_ext}[^\/"]+))))"""",
    """exa_json_path=$.Company,exa_field_name=company""",
    """exa_regex=({app}Progress ShareFile)""",
    """exa_json_path=$.ItemName,exa_regex=([^,"]+,){3}({failure_reason}[^"]+)"""
  ]
  DupFields = [ "file_name->src_file_name" , "file_ext->src_file_ext" , "file_path->src_file_path"]
  ParserVersion = v1.0.0


}
```