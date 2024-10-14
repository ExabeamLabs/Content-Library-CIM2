#### Parser Content
```Java
{
Name = microsoft-azure-json-file-success-2
   Vendor = Microsoft
   ParserVersion = v1.0.0
   Conditions = [ """serviceType":""", """"blob""", """"operationName":""", """"category":""" ]
 
azure-classicblob-json = {
    Vendor = Microsoft
    Product = Azure Monitor
    ExtractionType = json
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
    Fields = [
      """exa_json_path=$..time,exa_field_name=time""",
      """exa_json_path=$..resourceId,exa_field_name=resource""",
      """exa_json_path=$..category,exa_field_name=operation_type""",
      """exa_json_path=$..operationName,exa_field_name=operation""",
      """exa_json_path=$..operationVersion,exa_field_name=operation_version""",
      """exa_json_path=$..schemaVersion,exa_field_name=schema_version""",
      """exa_json_path=$..statusCode,exa_field_name=result_code""",
      """exa_json_path=$..statusText,exa_field_name=result""",
      """exa_json_path=$..callerIpAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})+)(:({src_port}\d+))?"""
      """exa_json_path=$..correlationId,exa_field_name=correlation_id""",
      """exa_json_path=$..identity.type,exa_field_name=auth_type""",
      """exa_json_path=$..location,exa_field_name=region""",
      """exa_json_path=$..accountName,exa_field_name=storage_account""", 
      """exa_json_path=$..userAgentHeader,exa_field_name=user_agent""", 
      """exa_json_path=$..lastModifiedTime,exa_field_name=file_modify_time""", 
      """exa_json_path=$..requestBodySize,exa_field_name=bytes_in""", 
      """exa_json_path=$..uri,exa_field_name=file_path""",
      """exa_json_path=$..uri,exa_regex=({url}({file_path}[^"]+\\/({file_name}[^\\?"]+))[^"]*|[^"]+)""",
      """exa_json_path=$..protocol,exa_field_name=protocol""",
      """exa_json_path=$..resourceType,exa_regex=({resource_type}({service_name}[^"\/]+)\/[^"]+)""",
      """exa_json_path=$..serviceType,exa_field_name=service_type"""      
    ]
    DupFields = [ "operation->operation_name", "region->location", "operation_type->category" 
}
```