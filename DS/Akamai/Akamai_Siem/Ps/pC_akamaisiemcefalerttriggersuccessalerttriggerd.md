#### Parser Content
```Java
{
Name = akamai-siem-cef-alert-trigger-success-alerttriggerd
Product = Akamai Siem
Vendor = Akamai
TimeFormat = "epoch"
Conditions = [ """CEF:""", """Akamai|akamai_siem""", """requestMethod=""", """ cs2Label=Rule""", """Vector Score:""", """Triggered Rules:""" ]
Fields = [
  """start=({time}\d+)"""
  """src=({src_ip}[A-Za-z\d.:]+)"""
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