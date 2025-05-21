#### Parser Content
```Java
{
Name = "vmware-carbonblackedr-cef-alert-trigger-success-watchlist"
Vendor = "VMware"
Product = "Carbon Black EDR"
TimeFormat = [ "epoch_sec", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ" ]
ExtractionType = json
Conditions = [
"""watchlist.hit"""
"""watchlist_name"""
]
Fields = [
"""exa_json_path=$.hostname,exa_regex=^({host}[\w\-.]+)$""",
"""exa_json_path=$.timestamp,exa_regex=({time}\d{10})""",
"""exa_json_path=$.created_time,exa_field_name=time""",
"""exa_json_path=$.type,exa_field_name=alert_type""",
"""exa_json_path=$.computer_name,exa_regex=^({dest_host}[\w\-.]+)$""",
"""exa_json_path=$.interface_ip,exa_regex=^({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?$""",
"""exa_json_path=$.username,exa_regex=^(({domain}[^\\"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)$""",
"""exa_json_path=$.sensor_id,exa_field_name=sensor_id""",
"""exa_json_path=$.md5,exa_field_name=hash_md5""",
"""exa_json_path=$.alert_severity,exa_field_name=alert_severity""",
"""exa_json_path=$.watchlist_name,exa_field_name=alert_name""",
"""exa_json_path=$.unique_id,exa_field_name=alert_id""",
"""exa_json_path=$.os_type,exa_field_name=os""",
"""exa_json_path=$.process_name,exa_field_name=process_name""",
"""exa_json_path=$.path,exa_regex=^({process_path}({process_dir}([^"]+)?[\\\/])?({process_name}[^\\\/"]+))$""",
"""exa_json_path=$.process_path,exa_regex=^({process_path}({process_dir}([^"]+)?[\\\/])?({process_name}[^\\\/"]+))$""",
"""exa_json_path=$.observed_filename,exa_regex=\[?"({process_path}({process_dir}([^"]+)?[\\\/])?({process_name}[^\\\/"]+))""",
"""exa_json_path=$.process_guid,exa_field_name=process_guid""",
"""exa_json_path=$.ioc_attr,exa_regex=({ioc}([^"\\]|(\\\\)*\\"|\\)+)""",
"""exa_json_path=$.ioc_value,exa_field_name=ioc""",
"""exa_json_path=$.parent_guid,exa_field_name=parent_process_guid""",
"""exa_json_path=$.parent_name,exa_field_name=parent_process_name""",
"""exa_json_path=$.cmdline,exa_field_name=process_command_line""",
"""exa_json_path=$.host_type,exa_field_name=host_type"""
]
DupFields = [
"process_path->path"
]
SOAR {
  IncidentType = "generic"
  DupFields = [
"""time->startedDate"""
"""vendor->source"""
"""rawLog->sourceInfo"""
"""alert_name->description"""
"""alert_severity->sourceSeverity"""
  ]
  NameTemplate = "Carbon Black Alert ${alert_name} found"
  ProjectName = "SOC"
  EntityFields = [
    {
      EntityType = "device"
      Name = "dest_address"
      Fields = [
"""dest_ip->ip_address"""
"""dest_host->host_name"""
      ]
    

}
```