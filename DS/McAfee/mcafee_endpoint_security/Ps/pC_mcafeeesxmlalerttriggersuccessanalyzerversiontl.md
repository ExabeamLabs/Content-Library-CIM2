#### Parser Content
```Java
{
Name = "mcafee-es-xml-alert-trigger-success-analyzerversion-tl"
    Vendor = "McAfee"
    Product = "McAfee Endpoint Security"
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<analyzername>"
      "<analyzerversion>"
      "<analyzer>"
    ]
    Fields = [
      "(?i)<(DetectedUTC|GMTTime)>({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)({host}[\\w\\-.]+)\\s+EPOEvents"
      "(?i)<TargetHostName>({src_host}[^<]+)"
      "(?i)<MachineName>({src_host}[^<]+)"
      "(?i)<IPAddress>(::1|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?)"
      "(?i)<SourceUserName>((NT-AUTORITÄT|AUTORIDADE NT|NT AUTHORITY|({domain}[^\\\\\\s]+))\\\\+)?((?i)system|({user}[^<\\\\\\s]+))<\\/SourceUserName>"
      "(?i)<DomainName>({domain}[^<]+)"
      "(?i)<UserName>((NT-AUTORITÄT|AUTORIDADE NT|NT AUTHORITY|({domain}[^\\\\\\s]+))\\\\+)?((?i)SYSTEM|({user}[^<\\\\\\s]+))<\\/UserName>"
      "(?i)<TargetUserName>((NT-AUTORITÄT|AUTORIDADE NT|NT AUTHORITY|({domain}[^\\\\\\s]+))\\\\+)?((?i)SYSTEM|({user}[^<\\\\\\s]+))<\\/TargetUserName>"
      "(?i)<ThreatCategory>({threat_category}[^<]+)"
      "(?i)<ThreatEventID>({event_code}[^<]+)"
      "(?i)<ThreatSeverity>({alert_severity}[^<]+)"
      "(?i)<ThreatCategory>({alert_name}[^<]+)"
      "(?i)<ThreatName>(-|_|(?i)none|({alert_name}[^<]+))<\\/ThreatName>"
      "(?i)<ThreatCategory>((?i)none|({alert_type}[^<]+))"
      "(?i)<ThreatType>((?i)none|({alert_type}[^<]+))"
      "(?i)<TargetFileName>({malware_url}[^=]*?[\\\\\\/]*\\s*({malware_file_name}[^\\s\\\\\\/<][^\\\\\\/<]*?))\\\\?<"
      "(?i)<AnalyzerDetectionMethod>({additional_info}[^<]+)"
      "(?i)<OSName>({os}[^<]+)"
      "(?i)<ThreatActionTaken>((?i)none|({action}[^<]+))<"
      "(?i)<AnalyzerName>(N\\/A|({event_name}[^<]+))"
      "(?i)<TaskName>({task_name}[^<]+)"
      "(?i)<TargetPath>({process_path}({process_dir}[^<]*?)\\s*(({process_name}[^\\s<\\\\\\/][^<\\\\\\/]*?)?))<"
      "(?i)<TargetName>\\s*({process_name}[^\\s<][^<]*?)<"
      "(?i)<SourceProcessName>({src_process_name}[^<]+)<"
      "(?i)<TargetHash>\\s*({hash_md5}[^\\s<][^<]*)<"
      "(?i)<Cleanable>({cleanable}[^<]+)<"
    ]
    SOAR {
      IncidentType = "malware"
      DupFields = [
        "time->startedDate"
        "vendor->source"
        "rawLog->sourceInfo"
        "event_code->sourceId"
        "alert_name->malwareName"
        "src_host->malwareVictimHost"
        "malware_url->malwareAttackerUrl"
        "alert_type->malwareCategory"
        "threat_category->malwareCategory"
        "alert_severity->sourceSeverity"
        "malware_file_name->malwareAttackerFile"
      ]
      NameTemplate = "McAfee EPO Alert ${alert_name} found"
      ProjectName = "SOC"
      EntityFields = [
        {
          EntityType = "device"
          Name = "src_address"
          Fields = [
            "src_ip->ip_address"
            "src_host->host_name"
          ]
        

}
```