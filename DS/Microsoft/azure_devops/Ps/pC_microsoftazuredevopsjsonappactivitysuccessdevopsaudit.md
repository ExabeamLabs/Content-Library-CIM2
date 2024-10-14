#### Parser Content
```Java
{
Name = microsoft-azuredevops-json-app-activity-success-devopsaudit
  ExtractionType = json
  Vendor = Microsoft
  Product = Azure DevOps
  ParserVersion = v1.0.0
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ" ]
  Conditions = [ """"eventType":"AzureDevOpsAuditEvent"""", """"subject":"AzureDevOps""", """"ActorUPN":"""" ]
  Fields = [ 
    """exa_json_path=$.data.Timestamp,exa_field_name=time"""
    """exa_json_path=$.eventType,exa_field_name=log_source"""
    """exa_json_path=$.topic,exa_field_name=resource_id"""
    """exa_json_path=$.subject,exa_field_name=app"""
    """exa_json_path=$.data.CategoryDisplayName,exa_field_name=category"""
    """exa_json_path=$.data.Details,exa_field_name=additional_info"""
    """exa_json_path=$.data.Data.result,exa_field_name=result_code"""
    """exa_json_path=$.data.Data.CallerProcedure,exa_field_name=operation"""
    """exa_json_path=$.data.Data.ConnectionName,exa_field_name=dest_service_name"""
    """exa_json_path=$.data.Data.DeploymentResult,exa_field_name=result"""
    """exa_json_path=$.data.Data.JobName,exa_field_name=action"""
    """exa_json_path=$.data.Data.EnvironmentName,exa_field_name=environment"""
    """exa_json_path=$.data.Area,exa_field_name=area_classification"""
    """exa_json_path=$.data.ActionId,exa_field_name=activity_id"""
    """exa_json_path=$.data.ActorDisplayName,exa_field_name=provider_name"""
    """exa_json_path=$.data.ActorUPN,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """exa_json_path=$.data.IpAddress,exa_field_name=src_ip"""
  ]


}
```