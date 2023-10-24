#### Parser Content
```Java
{
Name = mcafee-es-csv-alert-trigger-success-cleanfailed
    Vendor = McAfee
    Product = McAfee Endpoint Security
    ParserVersion = "v1.0.0"
    TimeFormat = "M/d/yyyy H:mm:ss a"
    Conditions = [ " (MD5)", " (Clean failed)"]
    Fields = [
      """({time}\d+/\d+/\d+\s+\d+:\d+:\d+ (am|AM|pm|PM)+)\t({additional_info}[^\t]+?)\s*\t(({domain}[^\t]+)(\\)+)?({user}[\w\.\-]{1,40}\$?)\t(\w+\[({process_id}\d+)\]|({process_path}[^\t]+))\t({malware_url}.+?\\({malware_file_name}[^\\]+))\t({alert_name}[^\t]+?)\s*\(({alert_type}[^\)]+)\)\t({hash_md5}\S+?)\s*\(MD5\)"""
    ]
    DupFields=[ "host->src_host" ]
    SOAR {
      IncidentType = "malware"
      DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "alert_name->malwareName", "src_host->malwareVictimHost", "malware_url->malwareAttackerUrl", "alert_type->malwareCategory", "malware_file_name->malwareAttackerFile"]
      NameTemplate = """McAfee EPO Alert ${alert_name} found"""
      ProjectName = "SOC"
      EntityFields = [
        {EntityType="device", Name ="src_address", Fields=["src_host->host_name"]

}
```