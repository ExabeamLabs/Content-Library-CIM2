#### Parser Content
```Java
{
Name = mcafee-dlp-kv-alert-trigger-success-destdns
  Vendor = McAfee
  Product = McAfee DLP Endpoint
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """IncidentId=""" , """src_device=""" , """dest_dns""" , """Policy"""]
  Fields = [
    """\Wtimestamp="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)""",
    """\Wsignature="*({alert_name}.+?)"""",
    """\WIncidentId="*({signature_id}\d+)""",
    """\Wevent_description="*({additional_info}.+?)"""",
    """\WDLP_FileName =?"*({file_name}.+?)"""",
    """\W(logon_)?user="*(N\/A|\s+|NULL|(({domain}[^\\]+)\\+)?({user}[\w\.\-]{1,40}\$?))"""",
    """\Wdest_dns="*({src_host}[^"]+)"""
    """\Wdest_nt_host="*({src_host}[^\s"]+)""",
    """\Wsrc_ip="*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\WPolicy="({policy_name}[^"]+)""",
    """\Wapp_file_name="({process_name}[^"]+)""",
    """app_prod_name="({app}[^"]+)""",
    """device_description="({device_id}[^"]+)"""

  ]
  ParserVersion = "v1.0.0"


}
```