#### Parser Content
```Java
{
Name = wazuh-w-cef-app-activity-success-wazuhalerts
  ParserVersion = "v1.0.0"
  Vendor = Wazuh
  Product = Wazuh
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = ["""|Wazuh|""" , """cat=wazuh"""]
  Fields = [
      """cs1=\(.+?\)\s*({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
      """\|({event_name}[^\|]+)\|\d+\|dvc=""",
      """msg=([^:]+:[^:]+:)?\s*'?({additional_info}.+?)(\.\s\w+:\s|'\.$|\.$)""",
  ]


}
```