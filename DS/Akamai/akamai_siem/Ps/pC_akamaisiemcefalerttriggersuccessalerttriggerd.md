#### Parser Content
```Java
{
Name = akamai-siem-cef-alert-trigger-success-alerttriggerd
Product = Akamai SIEM
Vendor = Akamai
TimeFormat = "epoch"
Conditions = [ """CEF:""", """Akamai|akamai_siem""", """requestMethod=""", """ cs2Label=Rule""", """Vector Score:""", """Triggered Rules:""" ]
Fields = [
  """start=({time}\d{13})"""
  """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """cs2=({alert_name}[^,=]+?)(,|\s*\w+=)"""
  """act=({result}[^=]+)\s+\w+="""
  """dhost=({web_domain}[^\s]+)\s+\w+="""
  """request=({malware_url}.+?)\s+\w+=""",
  """request=({malware_url}[^\s]+)\s+\w+="""
  """dpt=({src_port}\d+)"""
  """CEF:\d+\|([^\|]+\|){4}({alert_type}[^\|]+)"""
  """CEF:\d+\|([^\|]+\|){5}({alert_severity}\d+)\|"""
  """CEF:\d+\|([^\|]+\|){3}({action}[^\|]+)""",
]
ParserVersion = "v1.0.0"


}
```