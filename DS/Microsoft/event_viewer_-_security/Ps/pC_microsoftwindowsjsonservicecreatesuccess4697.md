#### Parser Content
```Java
{
Name = microsoft-windows-json-service-create-success-4697
  ExtractionType = json
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = ["epoch", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = [ """"event_id":""", """4697""", """A service was installed in the system""", """"provider":"Microsoft-Windows-Security-Auditing"""", """"message":""" ]
  Fields = [
  """exa_json_path=$.@timestamp,exa_field_name=time"""
  """exa_regex=({event_code}4697)"""
  """exa_json_path=$.host.hostname,exa_field_name=host"""
  """exa_regex=({event_name}A service was installed in the system)"""
  """exa_json_path=$.winlog.keywords,exa_field_name=result"""
  """exa_json_path=$.winlog.event_data.SubjectUserSid,exa_field_name=user_sid"""
  """exa_json_path=$.winlog.event_data.SubjectUserName,exa_field_name=user"""
  """exa_json_path=$.winlog.event_data.SubjectLogonId,exa_field_name=login_id"""
  """exa_json_path=$.winlog.event_data.ServiceName,exa_regex=(({service_name}[^"_]+)(_[^"<]+)?)"""
  """exa_json_path=$.winlog.event_data.ServiceFileName,exa_regex=(|({process_path}({process_dir}[^"]+[\\\/]+)?({process_name}[^"\\\/]+?)))"""
  """exa_json_path=$.winlog.event_data.ServiceType,exa_field_name=service_type"""
  """exa_json_path=$.winlog.event_data.ServiceStartType,exa_field_name=service_start_type"""
  """exa_json_path=$.winlog.event_data.ServiceServiceAccountStartType,exa_field_name=account_domain"""
  """exa_regex=Service File Name:\s*({process_command_line}[^=]+?)\s*(\\t|\\r|\\n)*Service Type:"""
  """exa_regex=Service File Name:\s+(|-|({process_path}({process_dir}[^\"=]+?[\\\/])?({process_name}[^\\\/\s]+)))\s*(\\t|\\n|\\r)*Service Type"""
  """exa_regex=Service File Name:\s*((?:[^\";]+)?[\\\/;])?({process_name}[^\\\/\";]+?\.[^\\\/\.;\"]+?)\s.*?\s*Service Type:"""
  """exa_regex=Service Account:\s*(|(({account_domain}[^\s"]+)\\)?({account_name}.+?))\s*(\"|$|<)"""
    ]
  DupFields = [ "host->dest_host", "process_command_line->service_command_line" ]
  ParserVersion = "v1.0.0"


}
```