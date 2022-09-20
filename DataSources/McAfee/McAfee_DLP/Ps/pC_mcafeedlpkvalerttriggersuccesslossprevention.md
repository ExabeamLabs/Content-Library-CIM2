#### Parser Content
```Java
{
Name = mcafee-dlp-kv-alert-trigger-success-lossprevention
  Vendor = McAfee
  Product = McAfee DLP
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """product="Data Loss Prevention"""", """signature_id="""", """is_laptop="""" ]
  Fields = [
    """\Wtimestamp="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)""",
    """\WDLP_IncidentId="*({alert_id}\d+)""",
    """\Wsignature="*({alert_name}.+?)"""",
    """\Wthreat_type="*({alert_type}.+?)"""",
    """\Wsignature_id="*({signature_id}\d+)""",
    """\Wseverity_id="*({alert_severity}\d+)""",
    """\Wevent_description="*({additional_info}.+?)"""",
    """\WDLP_FileName =?"*({file_name}.+?)"""",
    """\Wuser="*(N\/A|\s+|NULL|([^\\]+\\+)?({user}[^\s,"]+))"""",
    """\Wdest_nt_host="*({src_host}[^\s"]+)""",
    """\Wsrc_ip="*({src_ip}[A-Fa-f:\d.]+)""",
    """\Wprocess="*({process_path}({process_dir}(?:(\w+:)?[^:"]+)?[\\\/])?({process_name}[^\\"]+))""",
  ]
  ParserVersion = "v1.0.0"


}
```