#### Parser Content
```Java
{
Name = "fireeye-helix-json-alert-trigger-success-alerts"
  Vendor = "Trellix"
  Product = "Trellix Endpoint Security (HX)"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  ExtractionType = json
  Conditions = [ """"event_type":""", """"resolution":"ALERT"""", """"source":""", """"md5values":""", """"agent":""", """"indicator":""", """"is_false_positive":false""" ]
  Fields = [
    """exa_json_path=$.indicator.name,exa_field_name=indicator""",
    """exa_json_path=$.indicator.category,exa_field_name=category""",
    """exa_json_path=$.agent._id,exa_field_name=agent_id""",
    """exa_json_path=$.md5values[0],exa_field_name=hash_md5""",
    """exa_json_path=$.event_at,exa_field_name=time""",
    """exa_json_path=$.url,exa_field_name=url""",
    """exa_json_path=$.source,exa_field_name=alert_source""",
    """exa_json_path=$.resolution,exa_field_name=result""",
    """exa_json_path=$.event_id,exa_field_name=event_id"""
    """exa_json_path=$.event_type,exa_field_name=alert_type"""
    """exa_json_path=$..infection.infection-type,exa_field_name=alert_type"""
    """exa_json_path=$..infection.infection-name,exa_field_name=alert_name"""
    """exa_json_path=$.indicator.display_name,exa_field_name=alert_name"""
    """exa_json_path=$..confidence-level,exa_field_name=alert_severity""",
    """exa_json_path=$..actor-process.path,exa_field_name=process_path"""
    """exa_json_path=$..user.domain,exa_field_name=domain"""
    """exa_json_path=$..user.username,exa_field_name=user"""
    """exa_json_path=$..sub-type,exa_field_name=subtype"""
    """exa_json_path=$..file-event.file-path,exa_field_name=file_path"""
    """exa_json_path=$..os-details.$.name,exa_field_name=os"""
    """exa_json_path=$..action.result,exa_field_name=result"""
    """exa_regex=eventReason":\s*"({operation}[^"]+)""""
    """exa_regex=fileName":\s*"({file_name}[^"]+)""""
    """exa_regex=process":\s*"({process_name}[^"]+)""""
    """exa_regex="id":"({process_id}process[^"]+)""""
    """exa_regex=processCmdLine":\s*"({process_command_line}[^"]+)""""
    """exa_regex=processPath":\s*"({process_path}[^"]+)""""
    """exa_regex=(username|account_name)":\s*"(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
    """exa_regex=(filePath|file_path)":"({file_path}[^"]+)""""
    """exa_regex=fullPath":"({file_path}[^"]+)""""
    """exa_regex=(filePath|file_path).+?"name":"({file_name}[^"]+)""""
    """exa_regex=fileName":"({file_name}[^"]+)""""
    """exa_json_path=$..event_values[?(@.type == 'alert')].name,exa_field_name=alert_name"""
    """exa_json_path=$..event_values[?(@.type == 'alert')].alert_type,exa_field_name=alert_type"""
    """exa_json_path=$..event_values[?(@.type == 'alert')].description,exa_field_name=alert_description"""
    """exa_json_path=$..event_values[?(@.type == 'alert')].parameters.matched_rule,exa_field_name=rule"""
    """exa_json_path=$..event_values[?(@.type == 'eventlog')].extensions..categoryTechnique,exa_field_name=category"""
    """exa_json_path=$..event_values[?(@.type == 'process')].arguments,exa_field_name=process_command_line"""
    """exa_json_path=$..event_values[?(@.type == 'finding')].matched_rule..Name,exa_field_name=rule"""
    """exa_json_path=$..event_values[?(@.type == 'finding')].matched_rule..UUID,exa_field_name=rule_uid"""
    """exa_json_path=$..event_values[?(@.type == 'finding')].matched_rule..Desc,exa_field_name=rule_description"""
    """exa_json_path=$..event_values[?(@.type == 'finding')].matched_rule..Confidence,exa_field_name=alert_severity"""
    """exa_json_path=$..event_values[?(@.type == 'finding')].matched_rule..Mitre,exa_field_name=mitre_labels"""
    """exa_json_path=$..event_values[?(@.type == 'action')].name,exa_field_name=action"""
    """exa_json_path=$..event_values[?(@.type == 'event')].name,exa_field_name=event_name"""
  ]
  ParserVersion = "v1.0.0"


}
```