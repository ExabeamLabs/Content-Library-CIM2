#### Parser Content
```Java
{
Name = sysdig-monitor-json-alert-trigger-success-syscall
 ExtractionType = json
 ParserVersion = v1.0.0
 Vendor = Sysdig
 Product = Sysdig Monitor
 TimeFormat = "epoch_sec"
 Conditions = [ """"source":"syscall"""", """"originator":"policy"""", """"container""", """"category":"runtime"""",""""type":"policy"""" ]
 Fields = [
  """exa_json_path=$.timestamp,exa_field_name=time"""
  """exa_json_path=$.labels.['host.hostName'],exa_field_name=host"""
  """exa_json_path=$.labels.['host.mac'],exa_field_name=src_mac"""
  """exa_json_path=$.severity,exa_field_name=alert_severity"""
  """exa_json_path=$.description,exa_field_name=alert_name"""
  """exa_json_path=$.source,exa_field_name=alert_source"""
  """exa_json_path=$.content.fields.['user.name'],exa_field_name=user"""
  """exa_json_path=$.content.fields.['proc.name'],exa_field_name=process_name"""
  """exa_json_path=$.content.fields.['proc.cmdline'],exa_field_name=process_command_line"""
  """exa_json_path=$.content.fields.['proc.pid'],exa_field_name=process_id"""
  """exa_json_path=$.content.policyId,exa_field_name=policy_id"""
  """exa_json_path=$.content.ruleType,exa_field_name=rule_type"""
  """exa_json_path=$.content.ruleName,exa_field_name=rule"""
  """exa_json_path=$.content.fields.['container.id'],exa_field_name=container_id"""
  ]


}
```