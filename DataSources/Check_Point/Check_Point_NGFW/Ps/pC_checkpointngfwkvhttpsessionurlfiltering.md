#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-http-session-urlfiltering
  Vendor = Check Point
  Product = Check Point NGFW
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """product:\"URL Filtering\"""", """src_user_name:\"""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)\s+({host}[\w.\-]+)\s+CheckPoint\s""",
    """action:\\"({action}[^"\\]+)""",
    """src:\\"({src_ip}[^"\\]+)""",
    """dst:\\"({dest_ip}[^"\\]+)""",
    """resource:\\"({additional_info}[^"]+?)\\"""",
    """url=({url}(\w+://)?({web_domain}[^"\/:;]+)({uri_path}/[^"\?;]*?)({uri_query}\?[^";]*?)?)(\\"|;)""",
    """s_port:\\"({src_port}\d+)""",
    """src_machine_name:\\"({host}[^"\\@]+)(@({domain}\w+)?)""",
    """src_user_name:\\"({full_name}[^"\\\(]+?)\s*(\(|\\)""",
  ]
  ParserVersion = "v1.0.0"


}
```