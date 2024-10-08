#### Parser Content
```Java
{
Name = microsoft-azure-json-disk-write-success-disk
  ParserVersion = v1.0.0
  Conditions = [ """"operationName":""", """Microsoft.Compute/disks/write""" ]
  Fields = ${MSParserTemplates.azure-activity-json.Fields} [
    """exa_json_path=$.properties.responseBody,exa_regex="name\\?"+:\s*\\?"+({resource_name}[^"]+)\\"""
    """exa_json_path=$.properties.responseBody,exa_regex="location\\?"+:\s*\\?"+({region}[^"]+?)\\?""""
    """exa_json_path=$.properties.responseBody,exa_regex="managedBy\\?"+:\s*\\?"+({dest_host}[\w\-.]+)\\"""
    """exa_json_path=$.properties.responseBody,exa_regex="osType\\?"+:\s*\\?"+({os_type}[^"]+?)\\?""""
    """exa_json_path=$.properties.responseBody,exa_regex="createOption\\?"+:\s*\\?"+({source_resource_type}[^"]+?)\\?""""
    """exa_json_path=$.properties.responseBody,exa_regex="imageReference\\?"+:[^\}]+"+id\\?"+:\s*\\?"+({source_resource}[^"]+?)\\?""""
    """exa_json_path=$.properties.responseBody,exa_regex="creationData\\?"+:[^\}]+"+sourceResourceId\\?"+:\s*\\?"+({source_resource}[^"]+)\\"""
    """exa_json_path=$.properties.responseBody,exa_regex="diskSizeGB\\?"+:\s*\\?({disk_size}[^,"]+)"""
    """exa_json_path=$.properties.responseBody,exa_regex="diskState\\?"+:\s*\\?"+({disk_state}[^"]+?)\\?""""
  ]

azure-activity-json = {
    Vendor = Microsoft
    Product = Azure Monitor
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
    ExtractionType = json
    Fields = [
      """exa_json_path=$.eventTimestamp,exa_field_name=time""",
      """exa_json_path=$.time,exa_field_name=time""",
      """exa_json_path=$..authorization.scope,exa_field_name=authorization_scope""",
      """exa_json_path=$.caller,exa_regex=({email_address}[^"]+@({email_domain}[^"]+))""",
      """exa_json_path=$.callerIpAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})+)(:({src_port}\d+))?"""
      """exa_json_path=$..claims.ipaddr,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})+)(:({src_port}\d+))?"""
      """exa_json_path=$.correlationId,exa_field_name=correlation_id"""
      """exa_json_path=$.eventName.value,exa_regex=({operation_first}BeginRequest)"""
      """exa_json_path=$.eventName.value,exa_regex=({operation_last}EndRequest)"""
      """exa_json_path=$.category,exa_field_name=event_category"""
      """exa_json_path=$.category.value,exa_field_name=event_category"""
      """exa_json_path=$.operationName,exa_field_name=operation"""
      """exa_json_path=$.operationName.value,exa_field_name=operation"""
      """exa_json_path=$.operationName.localizedValue,exa_field_name=operation_name"""
      """exa_json_path=$.resourceGroupName,exa_regex=({resource_group}[^"]+)"""
      """exa_json_path=$.resourceProviderName.value,exa_field_name=service_name"""
      """exa_json_path=$.resourceType.value,exa_field_name=resource_type"""
      """exa_json_path=$.resourceId,exa_regex=({resource}({resource_path}[^"]+)\/({resource_name}[^"]+)|[^"]+)"""
      """exa_json_path=$.status.value,exa_field_name=status"""
      """exa_json_path=$.subscriptionId,exa_field_name=subscription_id"""
      """exa_json_path=$.tenantId,exa_field_name=tenant_id"""
      """exa_regex="resourceId":"({resource_id}(\/SUBSCRIPTIONS\/({subscription_id}[^\/]+))?(\/RESOURCEGROUPS\/({resource_group}[^\/]+))?\/[^"]+)""""
      
}
```