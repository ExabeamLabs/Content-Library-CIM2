#### Parser Content
```Java
{
Name = trendmicro-vone-json-alert-trigger-success-workbench
  Vendor = Trend Micro
  Product = Vision One
  ParserVersion = "v1.0.0"
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"investigationStatus":"""", """workbenchLink":""" ]
  Fields = [
    """exa_json_path=$.severity,exa_field_name=alert_severity""",
    """exa_json_path=$.status,exa_field_name=status_msg""",
    """exa_json_path=$.alertProvider,exa_field_name=alert_source""",
    """exa_json_path=$.createdDateTime,exa_field_name=time""",
    """exa_json_path=$.description,exa_field_name=description""",
    """exa_json_path=$.investigationResult,exa_field_name=result""",
    """exa_json_path=$.schemaVersion,exa_field_name=schema_version"""
    """exa_json_path=$..uuid,exa_field_name=alert_id""",
    """exa_json_path=$..workbenchLink,exa_field_name=url"""
    """exa_json_path=$..entities[*].entityValue,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
    """exa_json_path=$.indicators[?(@.type == 'email_sender')].value,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """exa_json_path=$.indicators[?(@.type == 'email_subject')].value,exa_field_name=email_subject""",
    """exa_json_path=$.indicators[?(@.type == 'email_message_id')].value,exa_regex=\<({message_id}[^"\>]+)"""
    """exa_json_path=$.id,exa_field_name=event_id""",
    """exa_json_path=$.model,exa_field_name=rule""",
    """exa_json_path=$.score,exa_field_name=original_risk_score"""
    """exa_json_path=$.matchedRules[0].name,exa_field_name=alert_name"""
    """exa_json_path=$.impactScope.entities[0][?(@.entityType == 'account')].entityValue,exa_regex=(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
    """exa_regex="entities":[^\$]+?"entityType":"host"[^\$]+?"entityValue":[^\$]+?"name":"({dest_host}[^,":]+)"""
  ]


}
```