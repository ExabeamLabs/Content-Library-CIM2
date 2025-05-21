#### Parser Content
```Java
{
Name = "microsoft-azure-json-image-write-success-imagewrite-1"
  Vendor = Microsoft
  Product = Azure Monitor
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
  ExtractionType = json
  Conditions = [ """"OperationNameValue":"MICROSOFT.COMPUTE/IMAGES/WRITE"""", """"Properties_d":""" ]
  Fields = [
    """exa_json_path=$.TimeGenerated,exa_field_name=time""",
    """exa_json_path=$.Authorization_d.scope,exa_field_name=authorization_scope""",
    """exa_json_path=$.Caller,exa_regex=({email_address}[^"]+@({email_domain}[^"]+))""",
    """exa_json_path=$.CallerIpAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})+)(:({src_port}\d+))?"""
    """exa_json_path=$.CorrelationId,exa_field_name=correlation_id"""
    """exa_json_path=$.Properties_d.eventCategory,exa_field_name=event_category"""
    """exa_json_path=$.Properties_d.entity,exa_regex=({resource}({resource_path}[^"]+)\/({resource_name}[^"]+)|[^"]+)"""
    """exa_json_path=$.ActivityStatusValue,exa_field_name=status_msg"""
    """exa_json_path=$.Properties_d.resourceGroup,exa_field_name=resource_group"""
    """exa_json_path=$.Properties_d.subscriptionId,exa_field_name=subscription_id"""
    """exa_json_path=$.ResourceProviderValue,exa_field_name=service_name"""
    """exa_json_path=$.OperationNameValue,exa_field_name=operation_name"""
  ]
  ParserVersion = "v1.0.0"


}
```