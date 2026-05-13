#### Parser Content
```Java
{
Name = microsoft-copilot-json-alert-trigger-success-dlprulematch
  Vendor = "Microsoft"
  Product = "Copilot"
  ExtractionType = json
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd HH:mm:ss.SSS","yyyy-MM-dd'T'HH:mm:ssZ"]
  Conditions = [ """Copilot""", """Protect sensitive M365 Copilot interactions""", """"Operation":"DlpRuleMatch"""", """"UserId":"""", """PolicyDetails":""" ]
  Fields = [
    """exa_json_path=$..CreationTime,exa_field_name=time"""
    """exa_json_path=$..Operation,exa_field_name=event_name"""
    """exa_json_path=$..Operation,exa_field_name=alert_type"""
    """exa_json_path=$..ApplicationName,exa_field_name=app"""
    """exa_json_path=$..UserId,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
    """exa_json_path=$..PolicyName,exa_field_name=alert_name"""
    """exa_json_path=$..PolicyName,exa_field_name=alert_subject"""
    """exa_json_path=$..SensitiveInformationTypeName,exa_field_name=rule_reason"""
    """exa_json_path=$..Actions,exa_field_name=rule_action"""
    """exa_json_path=$..RuleId,exa_field_name=rule_id"""
    """exa_json_path=$..PolicyId,exa_field_name=policy_id"""
    """exa_json_path=$..OSPlatform,exa_field_name=os"""
    """exa_json_path=$..DetectedValues[*].Value,exa_field_name=llm_request"""
    """exa_json_path=$..UserType,exa_field_name=user_type"""
    """"CreationTime":"({time}[^"]+)""""
    """"Operation":"({event_name}({alert_type}[^"]+))""""
    """"ApplicationName":"({app}[^"]+)""""
    """"UserId":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""""
    """"PolicyName":"({alert_subject}({alert_name}[^"]+))""""
    """"SensitiveInformationTypeName":"({rule_reason}[^"]+)""""
    """"Actions":\["({rule_action}[^"]+)"""
    """"RuleId":"({rule_id}[^"]+)""""
    """"PolicyId":"({policy_id}[^"]+)""""
    """"OSPlatform":"({os}[^"]+)""""
    """"DetectedValues":.+?"Value":"({llm_request}[^"]+)""""
    """"UserType"\s*:\s*"?({user_type}\d+)"""
  ]
    ParserVersion = "v1.0.0"


}
```