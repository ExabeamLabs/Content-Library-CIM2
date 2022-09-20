#### Parser Content
```Java
{
Name = mcafee-es-alert-trigger-success-4
    Vendor = McAfee
    Product = McAfee Endpoint Security
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """|Executable Fingerprint""", """|4|""" ]
    Fields = [
      """^[^|]*\|({time}\d+\-\d+\-\d+ \d+:\d+:\d+)""",
      """^([^|]*\|){3}({src_host}[^|]+)\|""",
      """^([^|]*\|){4}({src_ip}[a-fA-F0-9.:]+)""",
      """^([^|]*\|){5}(({domain}.+?)\\)?({user}[^\\|]+)\|""",
      """^([^|]*\|){6}({malware_url}.+?\\+({malware_file_name}[^\\|]+))\|""",
      """^([^|]*\|){11}({alert_type}[^|]+)\|""",
      """^([^|]*\|){12}({alert_type_id}\d+)""",
      """^([^|]*\|){13}({alert_name}[^|]+)\|""",
    ]
    SOAR {
      IncidentType = "malware"
      DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "alert_name->malwareName", "src_host->malwareVictimHost", "malware_url->malwareAttackerUrl", "alert_type->malwareCategory", "malware_file_name->malwareAttackerFile"]
      NameTemplate = """McAfee EPO Alert ${alert_name} found"""
      ProjectName = "SOC"
      EntityFields = [
        {EntityType="device", Name ="src_address", Fields=["src_ip->ip_address", "src_host->host_name"]

}
```