#### Parser Content
```Java
{
Name = "mcafee-es-xml-alert-trigger-success-analyzerversion"
    Vendor = McAfee
    Product = McAfee Endpoint Security
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [ """<AnalyzerName>""","""<AnalyzerVersion>""","""<Analyzer>""" ]
    Fields = [
	"""<(DetectedUTC|GMTTime)>({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
        """({host}[\w\-.]+)\s+EPOEvents""",
        """<TargetHostName>({src_host}[^<]+)""",
        """<MachineName>({src_host}[^<]+)""",
        """<IPAddress>(::1|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
        """<SourceUserName>((NT-AUTORITÄT|AUTORIDADE NT|NT AUTHORITY|({domain}[^\\\s]+))\\+)?((?i)system|({user}[\w\.\-\!\#\^\~]{1,40}\$?))<\/SourceUserName>""",
       """<DomainName>({domain}[^<]+)""",
       """<UserName>(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|((|NT AUTHORITY|NT-AUTORITÄT|AUTORIDADE NT|({domain}[^\\\s]+))\\+)?(|SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+(\w+=|$))<\/UserName>"""
       """<TargetUserName>((NT-AUTORITÄT|AUTORIDADE NT|NT AUTHORITY|({domain}[^\\\s]+))\\+)?((?i)SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))<\/TargetUserName>""",
       """<ThreatCategory>({threat_category}[^<]+)""",
       """<ThreatEventID>({event_code}[^<]+)""",
       """<ThreatSeverity>({alert_severity}[^<]+)""",
       """<ThreatCategory>({alert_name}[^<]+)""",
       """<ThreatName>(-|_|(?i)none|({alert_name}[^<]+))<\/ThreatName>"""
       """<ThreatCategory>((?i)none|({alert_type}[^<]+))""",
       """<ThreatType>((?i)none|({alert_type}[^<]+))""",
       """<TargetFileName>({malware_url}[^=]*?[\\\/]*\s*({malware_file_name}[^\s\\\/<][^\\\/<]*?))\\?<""",
       """<AnalyzerDetectionMethod>({additional_info}[^<]+)""",
       """<OSName>({os}[^<]+)""",
       """<ThreatActionTaken>((?i)none|({result}[^<]+))<""",
       """<AnalyzerName>(N\/A|({event_name}[^<]+))""",
       """<TaskName>({task_name}[^<]+)""",
       """<TargetPath>({process_path}({process_dir}[^<]*?)\s*(({process_name}[^\s<\\\/][^<\\\/]*?)?))<""",
       """<TargetName>\s*({process_name}[^\s<][^<]*?)<""",
       """<SourceProcessName>({src_process_name}[^<]+)<""",
       """<TargetHash>\s*({hash_md5}[^\s<][^<]*)<""",
       """<Cleanable>({cleanable}[^<]+)<""",
    ]
    SOAR {
      IncidentType = "malware"
      DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "event_code->sourceId", "alert_name->malwareName", "src_host->malwareVictimHost", "malware_url->malwareAttackerUrl", "alert_type->malwareCategory", "threat_category->malwareCategory", "alert_severity->sourceSeverity", "malware_file_name->malwareAttackerFile"]
      NameTemplate = """McAfee EPO Alert ${alert_name} found"""
      ProjectName = "SOC"
      EntityFields = [
        {EntityType="device", Name ="src_address", Fields=["src_ip->ip_address", "src_host->host_name"]

}
```