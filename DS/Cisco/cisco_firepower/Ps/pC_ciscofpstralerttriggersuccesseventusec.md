#### Parser Content
```Java
{
Name = "cisco-fp-str-alert-trigger-success-eventusec"
Vendor = "Cisco"
Product = "Cisco Firepower"
TimeFormat = "epoch_sec"
Conditions = [
  """archive_timestamp="""
  """event_usec="""
]
Fields = [
  """event_sec=({time}\d{10})"""
  """\sevent_id=({alert_id}\d+)\s+.+?class=({alert_name}(6|12|13|17|21))\s+priority=({alert_severity}\d+)\s+src_addr=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s+dst_addr=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
]
DupFields = [
  "alert_name->alert_type"
]
SOAR {
  IncidentType = "generic"
  DupFields = [
    "time->startedDate"
    "vendor->source"
    "rawLog->sourceInfo"
    "alert_name->description"
    "alert_severity->sourceSeverity"
  ]
  NameTemplate = "Cisco Sourcefire Alert ${alert_name} found"
  ProjectName = "SOC"
  EntityFields = [
    {
      EntityType = "device"
      Name = "src_address"
      Fields = [
        "src_ip->ip_address"
      ]
    

}
```