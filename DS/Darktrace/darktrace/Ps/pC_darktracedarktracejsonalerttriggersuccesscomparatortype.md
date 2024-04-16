#### Parser Content
```Java
{
Name = "darktrace-darktrace-json-alert-trigger-success-comparatortype"
Product = "Darktrace"
Vendor = "Darktrace"
TimeFormat = "epoch"
ExtractionType = json
Conditions = [
  """comparatorType"""
  """filterType"""
  """throttle"""
]
Fields = [
  """"+hostname"+:"+({src_host}[^"]+)"""
  """"+creationTime"+:({time}\d{13})"""
  """"+ip"+:"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"+breachUrl"+:"+({malware_url}[^"]+)"""
  """"+name"+:"+({alert_name}[^"]+)"""
  """"+macaddress"+:\"+({src_mac}[^"]+)"""
  """"+time"+:({time}.*?),"+model"""
  """"priority"+:({alert_severity}\d+)"""
  """"+typename"+:"+({alert_type}[^"]+)"""
  """"os"+:"+({os}[^"]+)"""
  """filterType"+:?"+Destination IP.+?value"+:"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"\}""",
  """"+description"+:"+({additional_info}[^"]+)"""
  """exa_json_path=$..hostname,exa_field_name=src_host"""
  """exa_json_path=$.creationTime,exa_field_name=time"""
  """exa_json_path=$..ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """exa_json_path=$.breachUrl,exa_field_name=malware_url"""
  """exa_json_path=$.model.name,exa_field_name=alert_name"""
  """exa_json_path=$..macaddress,exa_field_name=src_mac"""
  """exa_json_path=$.time,exa_field_name=time"""
  """exa_json_path=$..priority,exa_field_name=alert_severity"""
  """exa_json_path=$..typename,exa_field_name=alert_type"""
  """exa_json_path=$.os,exa_field_name=os"""
  """exa_json_path=$.value,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """exa_json_path=$.model.description,exa_field_name=additional_info"""
]
ParserVersion = "v1.0.0"


}
```