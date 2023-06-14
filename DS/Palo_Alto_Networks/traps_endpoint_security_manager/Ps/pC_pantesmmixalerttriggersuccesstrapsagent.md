#### Parser Content
```Java
{
Name = pan-tesm-mix-alert-trigger-success-trapsagent
  Vendor = Palo Alto Networks
  Product = Traps Endpoint Security Manager
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """|Palo Alto Networks|Traps Agent|""","""Prevention Key:""" ]
  Fields = [
    """\d\d:\d\d:\d\d ({host}[^\s]+)\sCEF""",
    """(devTime|rt)=({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d)""",
    """duser=(({domain}[^\\]+)\\)?(?: |({user}.+?))\s*\w+=""",
    """dhost=(?: |({src_host}.+?))\s*\w+=""",
    """\|Palo Alto Networks\|([^|]+\|){2}({alert_name}[^|]+)""",
    """\|Palo Alto Networks\|([^|]+\|){4}({alert_severity}[^|]+)""",
    """(subtype|cs2)=(?: |({alert_type}.+?))\s*\w+=""",
    """Prevention Key: (?: |({alert_id}.+?))\s*($|\w+=)""",
    """deviceProcessName =(?: |({malware_url}.+?))\s*\w+=""",
    """msg=(?: |({additional_info}.+?))(\.|:)"""
    """\sdst=({dest_ip}\d+\.\d+\.\d+\.\d+)\s"""
    """\ssrc=({src_ip}\d+\.\d+\.\d+\.\d+)\s""",
    """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
  ]
  SOAR {
    IncidentType = "malware"
    DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "alert_name->malwareName", "alert_severity->sourceSeverity", "alert_id->sourceId", "src_host->malwareVictimHost", "alert_type->description", "malware_url->malwareAttackerUrl"]
    NameTemplate = """Palo Alto Alert ${alert_name} found"""
    ProjectName = "SOC"
    EntityFields = [
      {EntityType="device", Name ="src_address", Fields=["src_host->host_name"]

}
```