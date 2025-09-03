#### Parser Content
```Java
{
Name = "mysql-m-json-database-activity-success-auditlog"
Vendor = "Mysql"
Product = "Mysql"
TimeFormat = "yyyyMMdd HH:mm:ss"
ExtractionType = json
ParserVersion = "v1.0.0"
Conditions = [ """"type":"mysql-audit"""", """"app":"mysql"""" ]
Fields = [
  """exa_json_path=$.beat.hostname,exa_field_name=host"""
  """exa_json_path=$.app,exa_field_name=app"""
  """exa_json_path=$.host.os.name,exa_field_name=os"""
  """exa_json_path=$.meta.cloud.provider,exa_field_name=provider_name"""
  """exa_json_path=$.meta.cloud.region,exa_field_name=region"""
  """exa_json_path=$.meta.cloud.machine_type,exa_field_name=machine_type"""
  """exa_json_path=$.message,exa_regex=({additional_info}({time}\d\d\d\d\d\d\d\d \d\d:\d\d:\d\d),({host}[^,]+),({event_name}[^,]+),({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})),([^,]+,){2}({connection_status}[^,]+),[^\$"]+)"""
  """exa_json_path=$.host.ip,exa_field_name=host_ip"""
]


}
```