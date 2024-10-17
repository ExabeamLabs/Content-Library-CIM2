#### Parser Content
```Java
{
Name = "vmware-carbonblackedr-json-alert-trigger-success-feed"
Vendor = "VMware"
Product = "Carbon Black EDR"
TimeFormat = "epoch_sec"
ExtractionType = json
Conditions = [
  """"type":"feed."""
  """"cb_server":""""
]
Fields = [
  """exa_regex=timestamp\"\s*:\s*\"?({time}\d{10})"""
  """exa_json_path=$.hostname,exa_field_name=host"""
  """exa_json_path=$.type,exa_field_name=alert_type"""
  """exa_json_path=$.computer_name,exa_field_name=dest_host"""
  """exa_json_path=$.interface_ip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """exa_json_path=$.docs[*].username,exa_regex=(({domain}[^\\\"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """exa_json_path=$.sensor_id,exa_field_name=sensor_id"""
  """exa_json_path=$.docs[*].process_md5,exa_field_name=hash_md5"""
  """exa_json_path=$.docs[*].unique_id,exa_field_name=alert_id"""
  """exa_json_path=$.docs[*].os_type,exa_field_name=os"""
  """exa_json_path=$.docs[*].process_name,exa_field_name=process_name"""
  """exa_json_path=$.docs[*].path,exa_regex=({process_path}({process_dir}([^\"]+)?[\\\/])?({process_name}[^\\\/\"]+))"""
  """exa_json_path=$.process_guid,exa_field_name=process_guid"""
  """exa_json_path=$.ioc_query_string,exa_field_name=ioc"""
  """exa_json_path=$.docs[*].parent_guid,exa_field_name=parent_process_guid"""
  """exa_json_path=$.docs[*].parent_name,exa_field_name=parent_process_name"""
  """exa_json_path=$.docs[*].cmdline,exa_field_name=process_command_line"""
  """exa_json_path=$.docs[*].host_type,exa_field_name=host_type"""
]
DupFields = [
  "process_path->path"
  "ioc->alert_name"
]
SOAR {
  IncidentType = "generic"
  DupFields = [
    "time->startedDate"
    "vendor->source"
    "rawLog->sourceInfo"
    "alert_name->description"
  ]
  NameTemplate = "Carbon Black Alert ${alert_name} found"
  ProjectName = "SOC"
  EntityFields = [
    {
      EntityType = "device"
      Name = "dest_address"
      Fields = [
        "dest_ip->ip_address"
        "dest_host->host_name"
      ]
    

}
```