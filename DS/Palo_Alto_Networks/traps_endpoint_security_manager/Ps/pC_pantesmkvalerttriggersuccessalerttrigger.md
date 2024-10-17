#### Parser Content
```Java
{
Name = pan-tesm-kv-alert-trigger-success-alerttrigger
Vendor = Palo Alto Networks
Product = Traps Endpoint Security Manager
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """Palo[Alto] TrapsAgent:"""
  """event from Computer:"""
  """Prevention Key:"""
]
Fields = [
  """\w+ \d\d \d\d:\d\d:\d\d ({host}[^\s]+)\s*Palo"""
  """User: (({domain}[^\\]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """eventID=({alert_name}[^\s]+) \w+="""
  """Module Name: ({alert_type}[^,]+),"""
  """sev=({alert_severity}\d+)"""
  """Prevention Key: ({alert_id}[^\s]+) \w+="""
  """Process Name: ({malware_url}[^,]+),""",
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
  ]
  NameTemplate = "Palo Alto Alert ${alert_name} found"
  ProjectName = "SOC"
  EntityFields = [
    {
      EntityType = "device"
      Name = "src_address"
      Fields = [
        "src_host->host_name"
      ]
    

}
```