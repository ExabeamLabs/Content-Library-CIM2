#### Parser Content
```Java
{
Name = microsoft-copilot-json-ai-agent-request-success-interaction
  Vendor = Microsoft
  Product = Copilot
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ssZ"]
  ExtractionType = json
  Conditions = [ """"Operation":"CopilotInteraction"""", """"Workload":"Copilot"""", """"CopilotEventData":""" ]
  Fields = [
    """exa_json_path=$..Operation,exa_field_name=event_name"""
    """exa_json_path=$..CreationTime,exa_field_name=time"""
    """exa_json_path=$..ClientIP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$..UserId,exa_regex=({email_address}[A-Za-z0-9!#$%&'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
    """exa_json_path=$..CopilotEventData.AppHost,exa_field_name=app"""
    """exa_json_path=$..UserType,exa_field_name=user_type"""
    """exa_json_path=$..AppIdentity,exa_field_name=app_type"""
    """exa_json_path=$..CopilotEventData.AccessedResources[0].SiteUrl,exa_field_name=url"""
    """exa_json_path=$..CopilotEventData.AccessedResources[0].Action,exa_field_name=access"""
    """exa_json_path=$..CopilotEventData.AccessedResources[0].Action,exa_field_name=action"""
    """exa_json_path=$..CopilotEventData.AccessedResources[*].Action,exa_field_name=allowed_data_actions"""
    """exa_json_path=$..AccountDisplayName,exa_field_name=full_name"""
    """exa_json_path=$..UserKey,exa_field_name=user_id"""
    """exa_json_path=$..CopilotEventData.Messages[?(@.isPrompt==true)].Id,exa_field_name=message_id"""
    """exa_json_path=$..CopilotEventData.AccessedResources[*].Type,exa_field_name=resource_type"""
    """exa_json_path=$..CopilotEventData.AccessedResources[*].Id,exa_field_name=resource_id"""
    """exa_json_path=$..CopilotEventData.AccessedResources[*].Name,exa_field_name=resource_name"""
    """exa_json_path=$..CopilotEventData.AccessedResources[*].Action,exa_field_name=operation_type"""
    """exa_json_path=$..CopilotEventData.AISystemPlugin[*].Name,exa_field_name=ai_tool_name"""
    """exa_json_path=$..CopilotEventData.ThreadId,exa_field_name=conversation_id"""
    """exa_json_path=$..CopilotEventData.ModelTransparencyDetails[*].ModelName,exa_field_name=model_name"""
    """exa_json_path=$..CopilotEventData.Messages[?(@.isPrompt==true)].JailbreakDetected,exa_field_name=blocked"""
    """"Operation"\s*:\s*"({event_name}[^",]+)""""
    """"CreationTime"\s*:\s*({time}[^"]+)""""
    """"ClientIP"\s*:\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
    """"UserId"\s*:\s*"(({email_address}[A-Za-z0-9!#$%&'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
    """"AccountDisplayName"\s*:\s*"({full_name}[^"]+)""""
    """"UserKey"\s*:\s*"({user_id}[\w\.\-\!\#\^\~]{1,40}\$?)""""
    """"AppHost"\s*:\s*"({app}[^",]+)""""
    """"UserType"\s*:\s*"?({user_type}\d+)"""
    """"AppIdentity"\s*:\s*"({app_type}[^",]+)""""
    """"SiteUrl"\s*:\s*"({url}[^",]+)""""
    """"Messages"\s*:\s*.+?"Id"\s*:\s*"({message_id}[^"]+)""""
    """"AccessedResources"\s*:\s*.+?"Type"\s*:\s*"({resource_type}[^"]+)""""
    """"AccessedResources"\s*:\s*.+?"Id"\s*:\s*"({resource_id}[^"]+)""""
    """"AccessedResources"\s*:\s*.+?"Name"\s*:\s*"({resource_name}[^"]+)""""
    """"Action"\s*:\s*"({action}({access}[^",]+))""""
    """"AISystemPlugin"\s*:.+?"Name"\s*:\s*"({ai_tool_name}[^"]+)""""
    """"ThreadId"\s*:\s*"({conversation_id}[^"]+)""""
    """"ModelName"\s*:\s*"({model_name}[^"]+)""""
    """"JailbreakDetected"\s*:\s*({blocked}true|false)"""
    ]
  ParserVersion = "v1.0.0"


}
```