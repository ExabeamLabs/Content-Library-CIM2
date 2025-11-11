#### Parser Content
```Java
{
Name = mcafee-epo-xml-alert-trigger-success-1027
  Vendor = Trellix
  Product = Trellix ePolicy Orchestrator
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """EPOEvents""", """<EventID>1027""", """MachineName>""" ]
  Fields = [
    """\d+\s+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\S*\s+({host}[\w\-.]+)\s+\w+""",
    """<MachineName>({src_host}[^<]+)<\/MachineName>""",
    """<IPAddress>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?<\/IPAddress>""",
    """<UserName>({domain}[^\\]+)\\({user}[\w\.\-\!\#\^\~]{1,40}\$?)<\/UserName>""",
    """<EventID>({event_code}[^<]+)<\/EventID>""",
    """<Severity>({alert_severity}[^<]+)<\/Severity>""",
    """<FileName>({file_dir}[^<]+[\\\/]+)({file_name}[^<]+?\.({file_ext}[^<]+)?)""",
    """<szVirusType>({alert_name}({alert_type}[^<]+))<\/szVirusType>""",
    """<MD5>({hash_md5}[^<]+)<\/MD5>""",
  ]


}
```