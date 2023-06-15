#### Parser Content
```Java
{
Name = mcafee-es-str-alert-trigger-success-epolicy
    Vendor = McAfee
    Product = McAfee Endpoint Security
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = ["""%ePolicy-""", """VIRUSCAN""" ]
    Fields = [
      """({alert_id}[^\s\^]+)[\s\^]+({host}[^\^\s]+)[\s\^]+({time}\d{4}-\d{2}-\d{2}\s\d{2}:\d{2}:\d{2}).+?({alert_type}(?:hip|av|fw)\.\w+)[\s\^]+\d+[\s\^]+\d+[\s\^]+({alert_name}BO\:(Stack|Writable BO:Heap|Image|Memory)|[^\:\^]+)""",
      """VIRUSCAN\d+[\s\^]+VirusScan Enterprise[\s\^]+\d+\.\d+[\s\^]+({src_host}[^\s\^]+)[\s\^]+(?:(?!\(null\))({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)?""",
      """(?:OAS|ODS)(?:[\^\s]+[^\^\s]+){4}[\s\^]+(?:[\s\w]+\\)?({user}[^\^\s]+)"""
    ]
    SOAR {
      IncidentType = "malware"
      DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "alert_id->sourceId", "alert_name->malwareName", "src_host->malwareVictimHost", "alert_type->malwareCategory"]
      NameTemplate = """McAfee EPO Alert ${alert_name} found"""
      ProjectName = "SOC"
      EntityFields = [
        {EntityType="device", Name ="src_address", Fields=["src_ip->ip_address", "src_host->host_name"]

}
```