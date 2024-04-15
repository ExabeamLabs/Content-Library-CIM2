#### Parser Content
```Java
{
Name = "checkpoint-es-kv-alert-trigger-success-monitor"
Vendor = "Check Point"
Product = "Check Point Endpoint Security"
TimeFormat = "epoch_sec"
Conditions = [
  """|product=SmartDefense|"""
  """|action=monitor|"""
]
Fields = [
  """date=({time}\d{10});"""
  """\|Protection Name =({alert_name}[^\|]+)\|"""
  """\|Attack Info=({alert_type}[^\|]+)\|"""
  """\|Severity=({alert_severity}[^\|]+)\|"""
  """\|src=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\|s_port=({src_port}\d+)"""
  """\|dst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\|service=({dest_port}\d+)"""
  """\|src_country=(?:Internal|({src_country}[^\|]+))\|"""
  """\|dst_country=(?:Other|({dest_country}[^\|]+))\|"""
  """\|src_user_name=[^(]+\(({user}[^)]+)"""
  """\|user=[^(]+\(({user}[^)]+)"""
]
ParserVersion = "v1.0.0"


}
```