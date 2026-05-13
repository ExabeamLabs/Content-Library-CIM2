#### Parser Content
```Java
{
Name = microsoft-copilot-json-ai-agent-powerplatform-catchall
  Vendor = Microsoft
  Product = Copilot
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ssZ"]
  Conditions = [ """"Operation":"Bot""", """"Workload":""", """"ResultStatus":""", """"PropertyCollection":""", """bot.schema""" ]
  ExtractionType = json
  Fields = [
    """exa_json_path=$..CreationTime,exa_field_name=time"""
    """exa_json_path=$..Operation,exa_field_name=operation"""
    """exa_json_path=$..Operation,exa_field_name=event_name"""
    """exa_json_path=$..ResultStatus,exa_field_name=result"""
    """exa_json_path=$..EnvironmentId,exa_field_name=workspace_id"""
    """exa_json_path=$..UserType,exa_field_name=user_type"""
    """exa_json_path=$..PropertyCollection[?(@.Name == 'powerplatform.analytics.resource.bot.schema.name')].Value,exa_field_name=ai_agent_name"""
    """exa_json_path=$..PropertyCollection[?(@.Name == 'powerplatform.analytics.resource.bot.id')].Value,exa_field_name=ai_agent_id"""
    """exa_json_path=$..UserId,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user_id}([\w\.\-\!\#\^\~]{1,40}\$?)))"""
    """exa_json_path=$..UserKey,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user_upn}([\w\.\-\!\#\^\~]{1,40}\$?)))"""
    """exa_json_path=$..PropertyCollection[?(@.Name == 'enduser.principal_name')].Value,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
    """exa_json_path=$..AccountDisplayName,exa_field_name=full_name"""
    """"CreationTime"\s*:\s*"({time}[^"]+)""""
    """"Operation"\s*:\s*"({operation}({event_name}[^"]+))""""
    """"ResultStatus"\s*:\s*"({result}[^"]+)""""
    """"EnvironmentId"\s*:\s*"({workspace_id}[^"]+)""""
    """"UserType"\s*:\s*"?({user_type}\d+)"""
    """"AccountDisplayName"\s*:\s*"({full_name}[^"]+)""""
    """"UserId"\s*:\s*"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user_id}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """"enduser.principal_name\\?":\s*\\?"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user_id}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """"powerplatform.analytics.resource.bot.schema.name\\?"\s*:\s*\\?"({ai_agent_name}[^"\\]+)\\?""""
    """"powerplatform.analytics.resource.bot.id\\?"\s*:\s*\\?"({ai_agent_id}[^"\\]+)\\?""""
  ]
  ParserVersion = "v1.0.0"


}
```