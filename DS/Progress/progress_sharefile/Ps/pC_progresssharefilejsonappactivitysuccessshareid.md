#### Parser Content
```Java
{
Name = "progress-sharefile-json-app-activity-success-shareid"
  Vendor = "Progress"
  Product = "Progress ShareFile"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  ExtractionType = json  
  Conditions = [ """destinationServiceName =Progress ShareFile""", """"CreatorEmail":""", """"ShareID":""" ]
  Fields = [
    """exa_json_path=$.CreationDate,exa_field_name=time""",
    """exa_json_path=$.RecipientEmail,exa_field_name=target""",
    """exa_json_path=$.UploadFolderID,exa_field_name=object_id""",
    """exa_json_path=$.CreatorEmail,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """exa_json_path=$.ShareID,exa_field_name=additional_info""",
    """exa_regex="Name":\s*"({file_path}({file_dir}[^"]*?[\/]+)?({file_name}[^\/"]+?(\.({file_ext}[^\/"]+))?))"""",
    """exa_regex=({app}Progress ShareFile)"""
  ]
  DupFields = [ "file_name->src_file_name" , "file_ext->src_file_ext" , "file_path->src_file_path"]
  ParserVersion = v1.0.0


}
```