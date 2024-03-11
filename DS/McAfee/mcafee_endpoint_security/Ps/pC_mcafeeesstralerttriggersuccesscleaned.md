#### Parser Content
```Java
{
Name = mcafee-es-str-alert-trigger-success-cleaned
  ParserVersion = v1.0.0
  Vendor = McAfee
  Product = McAfee Endpoint Security
  TimeFormat = "M/d/yyyy H:mm:ss a"
  Conditions = [ """ (MD5)""", """ Cleaned"""]
  Fields = [
    """({time}\d+/\d+/\d+\s+\d+:\d+:\d+ (am|AM|pm|PM)+)\s({additional_info}[^\s]+?)\s*\s(({domain}[^\s]+)(\\)+)?({user}[^\s]+)\s({process_path}[^\s]+)\s({url}.+?\\({malware_file_name}[^\\]+))\s({alert_name}[^\s]+?)\s*\(({alert_type}[^\)]+)\)\s({hash_md5}\S+?)\s*\(MD5\)"""
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