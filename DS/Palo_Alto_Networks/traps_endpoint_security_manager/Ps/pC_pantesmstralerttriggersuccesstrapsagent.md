#### Parser Content
```Java
{
Name = pan-tesm-str-alert-trigger-success-trapsagent
Vendor = Palo Alto Networks
Product = Traps Endpoint Security Manager
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","MMM dd yyyy HH:mm:ss"]
Conditions = [
  """,Traps Agent,"""
  """Prevention Key:"""
]
Fields = [
  """\d+\s+\d{4}\-\d+\-\d+T\d+:\d+:\d+\.\d+Z(\-|\+)\d+:\d+\s+({host}(\d{1,3}\.){3}\d{1,3})"""
  """({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d),Traps Agent,"""
  """,Traps Agent,([^,]*,){2}(?:-|({alert_name}[^,]+)),(?:-|({src_host}[^,]+)),(({domain}[^\\]+)\\)?(?:-|({user}[\w\.\-\!\#\^\~]{1,40}\$?)),(|({additional_info}.+?))\s*Prevention Key:"""
  """Prevention Key:\s*({alert_id}[^,\s]+),(?:-|({alert_severity}\d+)),(?:-|({alert_type}[^,]+)),(?:-|({malware_url}[^,]+)),([^,]*,){2}(?:-|({dest_ip}(\d{1,3}\.){3}\d{1,3}))"""
  """Parent process:\s*({process_name}[^\.]+)""",
  """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
]
SOAR {
  IncidentType = "malware"
  DupFields = [
    "time->startedDate"
    "vendor->source"
    "rawLog->sourceInfo"
    "alert_name->malwareName"
    "alert_severity->sourceSeverity"
    "alert_id->sourceId"
    "src_host->malwareVictimHost"
    "alert_type->description"
    "malware_url->malwareAttackerUrl"
    "dest_ip->malwareAttackerIp"
  ]
  NameTemplate = "Palo Alto Alert ${alert_name} found"
  ProjectName = "SOC"
  EntityFields = [
    {
      EntityType = "device"
      Name = "src_address"
      Fields = [
        """src_host->host_name"""
      ]
    

}
```