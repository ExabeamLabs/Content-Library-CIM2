#### Parser Content
```Java
{
Name = mcafee-es-csv-process-create-fail-executiondenied
  Vendor = McAfee
  Product = McAfee Endpoint Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """<SCORevent_name>EXECUTION_DENIED""", """EPOEvents""" ]
  Fields = [
    """<GMTTime>({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)</GMTTime>""",
    """({host}[\w\-.]+)\s+EPOEvents""",
    """<SCORuser_name>(({domain}[^\\\/<>]+)[\\\/]+)?({user}[\w\.\-]{1,40}\$?)</SCORuser_name>""",
    """<SCORfile_name>({file_path}({file_dir}[^<>]*?[\\\/<>]+)?({file_name}[^\\\/<>]+?(\.({file_ext}\w+))?))</SCORfile_name>""",
    """<SCORprocess_name>({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^\\\/<>]+))</SCORprocess_name>""",
    """<SCORparent_process_name>({parent_process_path}({parent_process_dir}[^<>]*?[\\\/]+)?({parent_process_name}[^\\\/<>]+))</SCORparent_process_name>""",
    """<SCORdeny_reason>({failure_reason}.+?)</SCORdeny_reason>""",
    """<SCORfile_type>({file_type}.+?)</SCORfile_type>""",
    """<SCORfile_md5>({hash_md5}.+?)</SCORfile_md5>""",
    """<RawMACAddress>({src_mac}.+?)</RawMACAddress>""",
    """<MachineName>({src_host}.+?)</MachineName>""",
    """<SCORevent_name>({result}.+?)</SCORevent_name>""",
    """<IPAddress>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?</IPAddress>""",
    """<OSName>({os}.+?)</OSName>""",
  ]
  ParserVersion = "v1.0.0"


}
```