#### Parser Content
```Java
{
Name = "microsoft-sysmon-json-registry-create-success-valuesettask13"
  Vendor = "Microsoft"
  Product = "Sysmon"
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [
    """Microsoft-Windows-Sysmon"""
    """Registry value set"""
    """"Task":13"""
  ]
  Fields = [
    """\"Message\":\s*\"({operation}[^:]+)"""
    """\"Image\":\s*\"[\\?]*({file_path}({file_dir}[^\"]*?[\\\/]+)?({file_name}[^\"\\\/]+?(\.({file_ext}\w+))?))\""""
    """\"Hostname\":\s*\"({host}[\w\-.]+)"""
    """\"UtcTime\":\s*\"({time}\d\d\d\d\-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)"""
    """\"UserID\":\s*\"({user_sid}[^\"]+)"""
    """\"ProcessGuid\":\s*\"({process_guid}[^\"]+)"""
    """\"ProcessID\":\s*({process_id}\d+)"""
    """\"Task\":\s*({event_code}\d+)"""
    """\"RuleName\":\s*\"(-|({access}[^\"]+))"""
    """\"AccountName\":\s*\"((?i)SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """\"Domain\":\s*\"((?i)NT AUTHORITY|({domain}[^\"]+))"""
    """"TargetObject":\s*"({object}({registry_path}[^"]*?\\+({registry_key}[^"\\\/]+?)\\+({registry_value}[^\\"]+)))""""
    """"({log_name}Microsoft-Windows-Sysmon)"""
  ]
  DupFields = [
    "file_path->process_path"
    "host->dest_host"
    "file_name->process_name"
    "operation->event_name"
  ]
  ParserVersion = "v1.0.0"


}
```