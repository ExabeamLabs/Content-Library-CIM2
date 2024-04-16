#### Parser Content
```Java
{
Name = "cisco-fp-cef-alert-trigger-success-sourcefire"
Vendor = "Cisco"
Product = "Cisco Firepower"
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """|Sourcefire|Sourcefire Management Console eStreamer|"""
]
Fields = [
  """\srt=({time}\d{13})"""
  """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
  """\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\sdhost=({src_host}[^\s]+)"""
  """\sshost=({dest_host}[^\s]+)"""
  """\sdst=(?:0.0.0.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
  """\ssrc=(?:0.0.0.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""
  """\scategory=({additional_info}.+?)\s+(\w+=|$)"""
  """\sduser=({user}[\w\.\-]{1,40}\$?)\s+(\w+=|$)"""
  """\sexternalId=({alert_id}\d+)"""
  """\|Sourcefire\|[^|]*\|[^|]*\|[^|]*\|[^-|]+\-[^\s]+\s+({alert_name}[^|]+)\|"""
  """\|Sourcefire\|[^|]*\|[^|]*\|[^|]*\|({alert_type}[^-|]+\-[^\s]+)[^|]+\|"""
  """\|Sourcefire\|[^|]*\|[^|]*\|[^|]*\|[^|]*\|({alert_severity}[^|]+)"""
]
SOAR {
  IncidentType = "malware"
  DupFields = [
    "time->startedDate"
    "vendor->source"
    "rawLog->sourceInfo"
    "alert_name->malwareName"
    "alert_type->malwareCategory"
    "alert_severity->sourceSeverity"
    "src_host->malwareVictimHost"
    "dest_ip->malwareAttackerIp"
    "dest_ip->malwareAttackerIp"
  ]
  NameTemplate = "Cisco Sourcefire Alert ${alert_name} found"
  ProjectName = "SOC"
  EntityFields = [
    {
      EntityType = "device"
      Name = "src_address"
      Fields = [
        "src_ip->ip_address"
        "src_host->host_name"
      ]
    

}
```