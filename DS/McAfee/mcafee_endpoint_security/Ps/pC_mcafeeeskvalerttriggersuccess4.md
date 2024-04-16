#### Parser Content
```Java
{
Name = mcafee-es-kv-alert-trigger-success-4
    Vendor = McAfee
    Product = McAfee Endpoint Security
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """|Executable Fingerprint""", """|4|""" ]
    Fields = [
      """^[^|]*\|({time}\d+\-\d+\-\d+ \d+:\d+:\d+)""",
      """^([^|]*\|){3}({src_host}[^|]+)\|""",
      """^([^|]*\|){4}({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """^([^|]*\|){5}(({domain}.+?)\\)?({user}[\w\.\-]{1,40}\$?)\|""",
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