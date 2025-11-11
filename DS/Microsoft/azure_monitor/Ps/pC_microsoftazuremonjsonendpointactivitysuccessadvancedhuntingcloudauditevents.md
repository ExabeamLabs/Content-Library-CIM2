#### Parser Content
```Java
{
Name = microsoft-azuremon-json-endpoint-activity-success-advancedhuntingcloudauditevents
  Vendor = Microsoft
  Product = Azure Monitor
  ExtractionType = json   
  ParserVersion = v1.0.0
  Conditions = [ """ResourceId":""", """"category":""", """"AdvancedHunting-CloudAuditEvents"""" ]  
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Fields = [
    """exa_json_path=$.tenantId,exa_field_name=tenant_id""",
    """exa_json_path=$.operationName,exa_field_name=operation""",
    """exa_json_path=$.properties.RawEventData.operationName,exa_field_name=operation""",
    """exa_json_path=$.category,exa_field_name=category""",
    """exa_regex=ResourceId":\s*"({resource_id}(\/SUBSCRIPTIONS\/({subscription_id}[^\/]+))?(\/RESOURCEGROUPS\/({resource_group}[^\/]+))?(\/PROVIDERS\/({provider_name}[^\/]+))?\/[^"]+)"""",
    """exa_json_path=$.Category,exa_field_name=category""",
    """exa_json_path=$..RoleLocation,exa_field_name=region""",
    """exa_json_path=$.properties.RawEventData.eventTimestamp,exa_field_name=time""",
    """exa_json_path=$.properties.IPAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.properties.RawEventData.operationName,exa_field_name=operation""",
    """exa_json_path=$.properties.RawEventData.authorization,exa_regex=[^\]]+action\\?"[^,]+?"({action}[^,]+?)\\?""""
    """exa_json_path=$.properties.RawEventData.authorization,exa_regex=[^\]]+role\\?"[^,]+?"({role}[^,]+?)\\?""""      
    """exa_json_path=$..EventName,exa_field_name=event_name""",
    """exa_json_path=$.properties.RawEventData.TaskName,exa_field_name=task_name""",
    """exa_json_path=$.properties.RawEventData.status,exa_field_name=result""",
    """exa_json_path=$.properties.RawEventData.eventSource,exa_field_name=service_name""",
    """exa_json_path=$.properties.AzureResourceId,exa_field_name=resource_id""",
    """exa_json_path=$.properties.Account,exa_field_name=account_name""",
    """exa_json_path=$.properties.RawEventData.ActionType,exa_field_name=action"""
  ]


}
```