#### Parser Content
```Java
{
Name = microsoft-copilot-json-ai-agent-request-success-interaction-2
  Vendor = Microsoft
  Product = Copilot
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ssZ"]
  ExtractionType = json
  Conditions = [ """"Operation": "CopilotInteraction"""", """"Workload": "Copilot"""", """"CopilotEventData":""" ]
  Fields = [
    """exa_json_path=$..Operation,exa_field_name=event_name"""
    """exa_json_path=$..CreationTime,exa_field_name=time"""
    """exa_json_path=$..ClientIP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$..UserId,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
    """exa_json_path=$..CopilotEventData.AppHost,exa_field_name=app"""
    """exa_json_path=$..UserType,exa_field_name=user_type"""
    """exa_json_path=$..AppIdentity,exa_field_name=app_type"""
    """exa_json_path=$..CopilotEventData.AccessedResources[0].SiteUrl,exa_field_name=url"""
    """exa_json_path=$..CopilotEventData.AccessedResources[0].Action,exa_field_name=access"""
    """exa_json_path=$..CopilotEventData.AccessedResources[*].Action,exa_field_name=allowed_data_actions"""
    """exa_json_path=$..AccountDisplayName,exa_field_name=full_name"""
    """"Operation"\s*:\s*"({event_name}[^",]+)""""
    """"CreationTime"\s*:\s*"({time}[^"]+)""""
    """"ClientIP"\s*:\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
    """"UserId"\s*:\s*"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
    """"AccountDisplayName"\s*:\s*"({full_name}[^"]+)""""
    """"AppHost"\s*:\s*"({app}[^",]+)""""
    """"UserType"\s*:\s*"?({user_type}\d+)"""
    """"AppIdentity"\s*:\s*"({app_type}[^",]+)""""
    """"SiteUrl"\s*:\s*"({url}[^",]+)""""
    """"Action"\s*:\s*"({access}[^",]+)""""
    ]
  ParserVersion = "v1.0.0"


}
```