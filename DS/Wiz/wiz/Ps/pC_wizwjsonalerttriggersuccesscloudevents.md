#### Parser Content
```Java
{
Name = wiz-w-json-alert-trigger-success-cloudevents
    Vendor = Wiz
    Product = Wiz
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    ExtractionType = json
    ParserVersion = "v1.0.0"
    Conditions = [ """"source":"CLOUD_EVENTS"""", """ruleId""", """severity""", """path"""", """type""", """hostInfo""", """eventExtraDetails""" ]
    Fields = [
       """exa_json_path=$.event.timestamp,exa_field_name=time""",
       """exa_json_path=$.event.commandLine,exa_field_name=process_command_line""",
       """exa_json_path=$.event.common.hostInfo.hostname,exa_field_name=host""",
       """exa_json_path=$.trigger.ruleId,exa_field_name=rule_id""",
       """exa_json_path=$.event.common.hostInfo.ips,exa_regex=[^,]+?,"({src_ip}(\d+\.){3}\d+)".*?]""",
       """exa_json_path=$.event.category,exa_field_name=alert_type""",
       """exa_json_path=$.event.severity,exa_field_name=alert_severity""",
       """exa_json_path=$.event.common.name,exa_field_name=alert_name""",
       """exa_json_path=$.event.timestamp,exa_field_name=time""",
       """exa_json_path=$.event.path,exa_regex=\s*({process_path}\[[^\]\\\{]+\])""",
       """exa_json_path=$.event.eventURL,exa_field_name=url""",
       """exa_json_path=$.event.source,exa_field_name=alert_source"""
    ]
  

}
```