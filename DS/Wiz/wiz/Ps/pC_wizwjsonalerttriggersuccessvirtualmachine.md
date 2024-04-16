#### Parser Content
```Java
{
Name = wiz-w-json-alert-trigger-success-virtualmachine
  Vendor = Wiz
  Product = Wiz
  ExtractionType = json
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """"type":"Created"""", """"severity":"""", """"name":"""", """"trigger":{"""", """"cloudPlatform":"""" ]
  Fields = [
    """exa_json_path=$.issue.created,exa_field_name=time""",
    """exa_json_path=$.control.id,exa_field_name=alert_id""",
    """exa_json_path=$.control.name,exa_field_name=alert_name""",
    """exa_json_path=$.resource.type,exa_field_name=alert_type""",
    """exa_json_path=$.control.severity,exa_field_name=alert_severity""",
    """exa_regex=({app}wiz)""",
    """exa_json_path=$.trigger.ruleName,exa_field_name=rule""",
    """exa_json_path=$.trigger.ruleId,exa_field_name=rule_id,exa_match_expr=!InList(toLower($.trigger.ruleId), "")""",
    """exa_json_path=$.resource.region,exa_field_name=region""",
    """exa_json_path=$.trigger.type,exa_field_name=operation""",
    """exa_json_path=$.control.description,exa_field_name=additional_info"""
  ]


}
```