#### Parser Content
```Java
{
Name = mcafee-es-str-alert-trigger-success-deleted
  ParserVersion = v1.0.0
  Vendor = McAfee
  Product = McAfee Endpoint Security
  TimeFormat = "M/d/yyyy\tH:mm:ss a"
  Conditions = [ """ (MD5)""", """ Deleted""" ]
  Fields = [
    """({time}\d+/\d+/\d+\s+\d+:\d+:\d+ (am|AM|pm|PM)+)\t({additional_info}[^\t]+?)\s*\t(({domain}[^\t]+)(\\)+)?({user}[^\t]+)\t({process_path}[^\t]+)\t({url}.+?\\({malware_file_name}[^\\]+))\t({alert_name}[^\t]+?)\s*\(({alert_type}[^\)]+)\)\t({hash_md5}\S+?)\s*\(MD5\)"""
  ]
  DupFields=[ "host->src_host" ]
  SOAR {
    IncidentType = "malware"
    DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "alert_name->malwareName", "src_host->malwareVictimHost", "url->malwareAttackerUrl", "alert_type->malwareCategory", "malware_file_name->malwareAttackerFile"]
    NameTemplate = """McAfee EPO Alert ${alert_name} found"""
    ProjectName = "SOC"
    EntityFields = [
      {EntityType="device", Name ="src_address", Fields=["src_host->host_name"]

}
```