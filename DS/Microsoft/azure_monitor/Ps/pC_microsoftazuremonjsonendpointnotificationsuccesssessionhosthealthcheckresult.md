#### Parser Content
```Java
{
Name = microsoft-azuremon-json-endpoint-notification-success-sessionhosthealthcheckresult
   ParserVersion = v1.0.0
   Conditions = [ """"SessionHostHealthCheckResult":""", """"TenantId":"""", """ResourceId":"""", """"_ItemId":"""" ]
   Fields = ${MSParserTemplates.microsoft-azure-endpoint-json.Fields}[
      """exa_json_path=$.Status,exa_field_name=status_msg""",
      """exa_json_path=$.SessionHostHealthCheckResult,exa_field_name=additional_info""",
      """exa_json_path=$.UpgradeState,exa_field_name=result"""
    ]
 
microsoft-azure-endpoint-json = {
    Vendor = Microsoft
    Product = Azure Monitor
    ExtractionType = json
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
    Fields = [
      """exa_json_path=$.TimeGenerated,exa_field_name=time""",
      """exa_json_path=$.ObjectName,exa_field_name=object""",
      """exa_json_path=$.InstanceName,exa_field_name=target""",
      """exa_json_path=$.TenantId,exa_field_name=tenant_id""",
      """exa_json_path=$.Computer,exa_field_name=host""",
      """exa_json_path=$.SourceSystem,exa_field_name=app""",
      """exa_regex=ResourceId":\s*"({resource_id}(\/SUBSCRIPTIONS\/({subscription_id}[^\/]+))?(\/RESOURCEGROUPS\/({resource_group}[^\/]+))?(\/PROVIDERS\/({provider_name}[^\/]+))?\/[^"]+)"""",
      """exa_regex="Command":\s*"\[?({process_command_line}.+?)\]",\s*"\w+":""",
      """exa_json_path=$.Category,exa_field_name=category""",
      """exa_json_path=$.RequestBodySize,exa_field_name=bytes_in""",
      """exa_json_path=$.ResponseBodySize,exa_field_name=bytes_out""",
      """exa_json_path=$.CallerIpAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})+)(:({src_port}\d+))?""",
      """exa_json_path=$.OperationName,exa_field_name=operation""",
      """exa_json_path=$.Protocol,exa_field_name=protocol""",
      """exa_json_path=$.Location,exa_field_name=region""",
      """exa_json_path=$.AuthenticationType,exa_field_name=auth_type""",
      """exa_json_path=$.SmbStatusCode,exa_field_name=result_code""",
      """exa_json_path=$.MetricResponseType,exa_field_name=result"""
    
}
```