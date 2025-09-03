#### Parser Content
```Java
{
Name = rubrik-cdm-json-app-success-cloudsummary
  Vendor = Rubrik
  Product = Rubrik Cloud Data Management
  TimeFormat =   [ "yyyy-MM-dd'T'HH:mm:ss.SSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ" ]
  ExtractionType = json
  Conditions = [ """"summary":"""", """"source":"Rubrik Security Cloud"""", """"custom_details":""", """"objectName":"""", """"eventName":"""" ]
  Fields = [
    """exa_json_path=$.timestamp,exa_field_name=time""",
    """exa_json_path=$..eventName,exa_field_name=event_name""",
    """exa_json_path=$..status,exa_field_name=result""",
    """exa_json_path=$.severity,exa_field_name=severity""",
    """exa_json_path=$..objectName,exa_field_name=object""",
    """exa_json_path=$..objectType,exa_field_name=object_type""",
    """exa_json_path=$..objectId,exa_field_name=object_id""",
    """exa_json_path=$.summary,exa_field_name=additional_info""",
    """exa_regex="summary":".*?Host\s*'(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({host}[\w\-\.]+))'""",
    """exa_json_path=$..errorCode,exa_field_name=error_code""",
    """exa_json_path=$..url,exa_field_name=url""",
    """exa_regex="location":"({host}[\w\-\.]+)"""
    """exa_regex="summary":".*?({failure_reason}({result}(?i)failed)[^"]+?)\.?""""
    """exa_regex="summary":".*?Reason:\s*({failure_reason}[^"]+?)\.?\s*""""
  ]
  DupFields = [ "host->dest_host", "object_type->app" ]
  ParserVersion = "v1.0.0"


}
```