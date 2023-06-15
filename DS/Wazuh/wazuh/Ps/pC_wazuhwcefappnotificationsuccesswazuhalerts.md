#### Parser Content
```Java
{
Name = wazuh-w-cef-app-notification-success-wazuhalerts
  ParserVersion = "v1.0.0"
  Vendor = Wazuh
  Product = Wazuh
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = ["""|Wazuh|""" , """cat=ossec"""]
  Fields = [
      """cs1=\(.+?\)\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
      """\|({event_name}[^\|]+)\|\d+\|dvc=""",
      """msg=([^:]+:[^:]+:)?\s*'?({additional_info}.+?)(\.\s\w+:\s|'\.$|\.$)""",
      """File[^:]*:\s*({file_path}({file_dir}[^\.]*?[\\\/]*)?(|({file_name}[^\\\/"]*?(\.({file_ext}[^\\\/\.\s"]*))?)))\."""
  ]


}
```