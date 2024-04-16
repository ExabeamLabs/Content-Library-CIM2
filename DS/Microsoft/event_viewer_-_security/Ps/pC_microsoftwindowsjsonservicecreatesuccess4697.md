#### Parser Content
```Java
{
Name = microsoft-windows-json-service-create-success-4697
  ExtractionType = json
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "epoch"
  Conditions = [ """"event_id":4697""", """A service was installed in the system""", """"provider":"Microsoft-Windows-Security-Auditing"""", """"message":""" ]
  Fields = [
    """exa_json_path=$.timestamp,exa_field_name=time"""
  """exa_regex=({event_code}4697)"""
  """exa_json_path=$.host.hostname,exa_field_name=host"""
  """exa_regex=({event_name}A service was installed in the system)"""
  """exa_json_path=$.winlog.keywords,exa_field_name=result"""
  """exa_json_path=$.winlog.event_data.SubjectUserSid,exa_field_name=user_sid"""
  """exa_json_path=$.winlog.event_data.SubjectUserName,exa_field_name=user"""
  """exa_json_path=$.winlog.event_data.SubjectLogonId,exa_field_name=login_id"""
  """exa_json_path=$.winlog.event_data.ServiceName,exa_field_name=service_name"""
  """exa_json_path=$.winlog.event_data.ServiceName,exa_field_name=service_name"""
  """exa_json_path=$.winlog.event_data.ServiceFileName,exa_regex=(|({process_path}({process_dir}[^"]+[\\\/]+)?({process_name}[^"\\\/]+?)))"""
   """exa_json_path=$.winlog.event_data.ServiceType,exa_field_name=service_type"""
  """exa_json_path=$.winlog.event_data.ServiceStartType,exa_field_name=service_start_type"""
   """exa_json_path=$.winlog.event_data.ServiceServiceAccountStartType,exa_field_name=account_domain"""
    ]
  DupFields = [ "host->dest_host" ]
  ParserVersion = "v1.0.0"


}
```