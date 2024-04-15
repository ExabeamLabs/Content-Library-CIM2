#### Parser Content
```Java
{
Name = "darktrace-darktrace-json-alert-trigger-success-comparatortype"
Product = "Darktrace"
Vendor = "Darktrace"
TimeFormat = "epoch"
Conditions = [
  """comparatorType"""
  """filterType"""
  """throttle"""
]
Fields = [
  """"+hostname"+:"+({src_host}[^"]+)"""
  """"+creationTime"+:({time}\d{13})"""
  """"+ip"+:"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"+breachUrl"+:"+({malware_url}[^"]+)"""
  """"+name"+:"+({alert_name}[^"]+)"""
  """"+macaddress"+:\"+({src_mac}[^"]+)"""
  """"+time"+:({time}.*?),"+model"""
  """"priority"+:({alert_severity}\d+)"""
  """"+typename"+:"+({alert_type}[^"]+)"""
  """"os"+:"+({os}[^"]+)"""
  """filterType"+:?"+Destination IP.+?value"+:"+({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"\}""",
  """"+description"+:"+({additional_info}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```