#### Parser Content
```Java
{
Name = mcafee-epo-xml-endpoint-notification-success-epoevents
    Vendor = McAfee
    Product = McAfee ePolicy Orchestrator
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SZ"
    Conditions = [ """ EPOEvents """, """<OSName>""" ]
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z) ({host}[\w.\-]+) EPOEvents -""",
      """<MachineName>({src_host}[^<]+)""",
      """<InitiatorType>(N\/A|({event_name}[^<]+))""",
      """<RawMACAddress>({src_mac}[a-fA-F\d.:]+)""",
      """<IPAddress>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """<OSName>({os}[^<]+)""",
      """<UserName>({last_name}[^\\<,]+),\s*({first_name}[^<,]+)<""",
      """<UserName>(N\/A|((NT-AUTORITÄT|AUTORIDADE NT|NT AUTHORITY|({domain}[^\\\s]+))\\+)?(SYSTEM|({user}[^<\\\s,]+)))<""",
      """<DomainName>({domain}[^<]+)""",
      """<EventID>({event_code}\d+)""",
      """<SiteName>(N\/A|({mcafee_sitename}[^<]+))""",
      """\sProductName =""?({product_name}[^"=]+)""",
      """\sProductFamily=""?({product_family}[^"=]+)""",
      """<ThreatName>(?:(-|_)|({alert_name}[^<]+))<\/ThreatName>""",
      """<ThreatType>({alert_type}[^<]+)""",
      """<TaskName>({task_name}[^<]+)""",
      """<TargetUserName>((NT-AUTORITÄT|AUTORIDADE NT|NT AUTHORITY|({domain}[^\\\s]+))\\+)?(SYSTEM|({user}[^<\\\s]+))<\/TargetUserName>""",
      """<TargetPath>({process_path}({process_dir}[^<]{0,2000}?)\s*(({process_name}[^\s<\\\/][^<\\\/]{0,2000}?)?))<""",
      """<TargetName>({process_name}[^<]+)""",
      """<SourceProcessName>({src_process_name}[^<]+)""",
      """<TargetHash>({hash_md5}[^<]+)""",
      """<Cleanable>({cleanable}[^<]+)""",
      """<RuleName>({rule}[^<]+)""",
      """<ProcessName>({process_name}[^<]+)""",
      """<FileName>({file_name}[^<]+)"""
    ]
  

}
```