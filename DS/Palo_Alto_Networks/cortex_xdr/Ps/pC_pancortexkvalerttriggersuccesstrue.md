#### Parser Content
```Java
{
Name = "pan-cortex-kv-alert-trigger-success-true"
Vendor = "Palo Alto Networks"
Product = "Cortex XDR"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """,alert,"""
  """,true,"""
]
Fields = [
  """"+\[\"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?.+?\"+\]\"+,([^,]*,){8}({user_sid}[^,]+),({domain}[^\\]+)\\(SYSTEM|({user}[^,]+))"""
  """"+\[\"+(?:[A-Fa-f\d:.]+).+?\"+\]\"+,([^,]*,){17}({file_path}({file_dir}[^\"][^,]*?[\\\/]+)?({file_name}[^\\\/]*?(\.({file_ext}\w+))?)),"""
  """,alert,([^,]*,){8}({alert_severity}[^,]+)"""
  """,alert,([^,]*,){14}({alert_name}[^,]+),({alert_type}[^,]+),\"*({additional_info}[^\"]+)\"*,"""
]
DupFields = [
  "file_name->malware_file_name"
]
ParserVersion = "v1.0.0"


}
```