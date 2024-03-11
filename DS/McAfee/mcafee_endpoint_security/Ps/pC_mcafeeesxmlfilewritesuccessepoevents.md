#### Parser Content
```Java
{
Name = mcafee-es-xml-file-write-success-epoevents
  ParserVersion = v1.0.0
  Vendor = McAfee
  Product = McAfee Endpoint Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """<SCORevent_name>WRITE_DENIED""", """EPOEvents""" ]
  Fields = [
    """<GMTTime>({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)</GMTTime>""",
    """({host}[\w\-.]+)\s+EPOEvents""",
    """<SCORuser_name>(({domain}[^\\\/<>]+)[\\\/]+)?({user}[^\\\/<>]+)</SCORuser_name>""",
    """<SCORfile_name>({file_path}({file_dir}[^<>]*?[\\\/<>]+)?({file_name}[^\\\/<>]+?(\.({file_ext}\w+))?))</SCORfile_name>""",
    """<SCORprocess_name>({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^\\\/<>]+))</SCORprocess_name>""",
    """<RawMACAddress>({src_mac}.+?)</RawMACAddress>""",
    """<MachineName>({src_host}.+?)</MachineName>""",
    """<SCORevent_name>({action}.+?)</SCORevent_name>""",
    """<IPAddress>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?</IPAddress>""",
    """<OSName>({os}.+?)</OSName>"""
  ]


}
```