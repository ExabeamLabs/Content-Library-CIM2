#### Parser Content
```Java
{
Name = microsoft-azuremon-json-app-activity-operationname
  Vendor = Microsoft
  Product = Azure Monitor
  ExtractionType = json
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"]
  Conditions = [ """"resourceId":""", """"operationName":""", """"category":""" ]
  Fields = [
    """exa_json_path=$.time,exa_field_name=time""",
    """exa_json_path=$.operationName,exa_field_name=operation""",
    """exa_json_path=$.category,exa_field_name=category""",
    """exa_json_path=$.resourceId,exa_field_name=resource_id""",
    """exa_json_path=$..correlationId,exa_field_name=correlation_id""",
    """exa_json_path=$.tenantId,exa_field_name=tenant_id""",
    """exa_json_path=$..resultType,exa_field_name=result_code""",
    """exa_json_path=$..resultSignature,exa_field_name=result""",
    """exa_json_path=$..callerIpAddress,exa_regex=^({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?$""",
    """exa_json_path=$..resultDescription,exa_regex=^\s*({additional_info}[^"]+?)\s*$""",
    """exa_json_path=$..caller,exa_field_name=user"""
  ]
  ParserVersion = v1.0.0


}
```