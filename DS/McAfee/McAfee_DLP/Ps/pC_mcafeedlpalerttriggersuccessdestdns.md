#### Parser Content
```Java
{
Name = mcafee-dlp-alert-trigger-success-destdns
  Vendor = McAfee
  Product = McAfee DLP
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """IncidentId=""" , """src_device=""" , """dest_dns""" , """Policy"""]
  Fields = [
    """\Wtimestamp="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)""",
    """\Wsignature="*({alert_name}.+?)"""",
    """\WIncidentId="*({signature_id}\d+)""",
    """\Wevent_description="*({additional_info}.+?)"""",
    """\WDLP_FileName =?"*({file_name}.+?)"""",
    """\W(logon_)?user="*(N\/A|\s+|NULL|(({domain}[^\\]+)\\+)?({user}[^\s,"]+))"""",
    """\Wdest_dns="*({src_host}[^"]+)"""
    """\Wdest_nt_host="*({src_host}[^\s"]+)""",
    """\Wsrc_ip="*({src_ip}[A-Fa-f:\d.]+)""",
    """\WPolicy="({policy_name}[^"]+)""",
    """\Wapp_file_name="({process_name}[^"]+)""",
    """app_prod_name="({app}[^"]+)""",
    """device_description="({device_id}[^"]+)"""

  ]
  ParserVersion = "v1.0.0"


}
```