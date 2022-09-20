#### Parser Content
```Java
{
Name = mcafee-epo-xml-alert-trigger-success-1027
  Vendor = McAfee
  Product = Mcafee EPO
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """EPOEvents""", """<EventID>1027""", """MachineName>""" ]
  Fields = [
    """\d+\s+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\S*\s+({host}[\w\-.]+)\s+\w+""",
    """<MachineName>({src_host}[^<]+)<\/MachineName>""",
    """<IPAddress>({src_ip}[^<]+)<\/IPAddress>""",
    """<UserName>({domain}[^\\]+)\\({user}[^<]+)<\/UserName>""",
    """<EventID>({event_code}[^<]+)<\/EventID>""",
    """<Severity>({alert_severity}[^<]+)<\/Severity>""",
    """<FileName>({file_dir}[^<]+[\\\/]+)({file_name}[^<]+?\.({file_ext}[^<]+)?)""",
    """<szVirusType>({alert_type}[^<]+)<\/szVirusType>""",
    """<MD5>({hash_md5}[^<]+)<\/MD5>""",
  ]
  DupFields = ["alert_type->alert_name"]
 

}
```