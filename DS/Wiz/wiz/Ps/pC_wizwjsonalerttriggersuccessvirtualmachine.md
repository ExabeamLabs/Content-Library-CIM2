#### Parser Content
```Java
{
Name = wiz-w-json-alert-trigger-success-virtualmachine
  Vendor = Wiz
  Product = Wiz
  ExtractionType = json
  ParserVersion = v1.0.0
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"]
  start_timeFormat="yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  end_timeFormat="yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """"type":"""", """"severity":"""", """"name":"""", """"trigger":{"""", """"cloudPlatform":"""" ]
  Fields = [
    """exa_json_path=$..created,exa_field_name=time""",
    """exa_json_path=$.control.id,exa_field_name=alert_id""",
    """exa_json_path=$.threat.id,exa_field_name=threat_id""",
    """exa_json_path=$.threat.title,exa_field_name=alert_name""",
    """exa_json_path=$.control.name,exa_field_name=alert_name""",
    """exa_json_path=$.threat.resources[0].type,exa_field_name=alert_type""",
    """exa_json_path=$.resource.type,exa_field_name=alert_type""",
    """exa_json_path=$.threat.severity,exa_field_name=alert_severity""",
    """exa_json_path=$.control.severity,exa_field_name=alert_severity""",
    """exa_regex=({app}wiz)""",
    """exa_json_path=$.trigger.ruleName,exa_field_name=rule""",
    """exa_json_path=$.trigger.ruleId,exa_field_name=rule_id,exa_match_expr=!InList(toLower($.trigger.ruleId), "")""",
    """exa_json_path=$.resource.region,exa_field_name=region""",
    """exa_json_path=$.trigger.type,exa_field_name=operation""",
    """exa_json_path=$.control.description,exa_field_name=additional_info""",
    """exa_json_path=$.threatId,exa_field_name=threat_id""",
    """exa_json_path=$..threatURL,exa_field_name=threat_url""",
    """exa_json_path=$..title,exa_field_name=alert_name""",
    """exa_json_path=$.description,exa_field_name=additional_info""",
    """exa_json_path=$.threat.description,exa_field_name=additional_info""",
    """exa_json_path=$.severity,exa_field_name=alert_severity""",
    """exa_json_path=$..mitreTactics,exa_field_name=tactic""",
    """exa_json_path=$..mitreTechniques,exa_field_name=technique""",
    """exa_json_path=$.timeframe.start,exa_field_name=start_time""",
    """exa_json_path=$.timeframe.end,exa_field_name=end_time""",
    """exa_json_path=$..actors[0].email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)""",
    #"""exa_json_path=$..actors[0].name,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)""",
    """exa_json_path=$..actors[?(@.type == 'Identity')].name,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """exa_json_path=$..actors[0].externalId,exa_field_name=external_id""",
    """exa_json_path=$.resources[0].externalId,exa_field_name=resource_id""",
    """exa_json_path=$.threat.resources[0].externalId,exa_field_name=resource_id""",
    """exa_json_path=$.resources[0].region,exa_field_name=region""",
    """exa_json_path=$.resources[0].type,exa_field_name=resource_type""",
    """exa_json_path=$.threat.resources[0].name,exa_field_name=resource_name""",
    """exa_json_path=$.threat.resources[0].type,exa_field_name=resource_type""",
    """exa_json_path=$..triggeringEvents[0].actorIP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """exa_json_path=$..triggeringEvents[0].category,exa_field_name=event_category""",
    """exa_json_path=$..triggeringEvents[0].eventTime,exa_field_name=time""",
    """exa_json_path=$..triggeringEvents[0].name,exa_field_name=event_name""",
    """exa_json_path=$..triggeringEvents[0].id,exa_field_name=event_id""",
    """exa_json_path=$..triggeringEvents[0].status,exa_field_name=state""",
    """exa_json_path=$.threat.created,exa_field_name=time""",
    """exa_json_path=$.threat.id,exa_field_name=threat_id""",
    """exa_json_path=$.threat.status,exa_field_name=state"""   
  ]


}
```