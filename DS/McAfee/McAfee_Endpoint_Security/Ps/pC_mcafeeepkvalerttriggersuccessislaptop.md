#### Parser Content
```Java
{
Name = mcafee-ep-kv-alert-trigger-success-islaptop
    ParserVersion = v1.0.0
    Vendor = McAfee
    Product = McAfee Endpoint Security
    TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
    Conditions = [ """timestamp=""", """signature_id""", """is_laptop""", """Data Loss Prevention""" ]
    Fields = [
      """timestamp="*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+)""",
      """AutoID="*({alert_id}\d+)""",
      """signature="*\s*(_|({alert_name}.+?))\s*"*,? threat_type""",
      """threat_type="*(\s|none|({alert_type}.+?))"*,? signature_id""",
      """signature_id="*({signature_id}\d+)""",
      """severity_id="*({alert_severity}\d+)""",
      """event_description="*({additional_info}[^"]+)""",
      """\Wprocess="*({process_path}({process_dir}(?:(\w+:)?[^:"]+)?[\\\/])?({process_name}[^\\"]+))""",
      """\slogon_user.+?user="*(N\/A|\s+|NULL|([^\\]+\\+)?({user}[^\s,"]+))""",
      """, username="+(N\/A|NULL|({user}[^,]+?))(|,.*?)"+,""",
      """src_dns="*({src_host}[^\s"]+)"""",
      """src_ip="({src_ip}[A-Fa-f:\d.]+)"""",
      """dest_dns="*({dest_host}[^\s"]+)"""",
      """dest_ip="*({dest_ip}[A-Fa-f:\d.]+)"""",
      """os="*({os}[^"]+)"""",
      """category="*({category}[^\s"]+)"""",
    ]


}
```