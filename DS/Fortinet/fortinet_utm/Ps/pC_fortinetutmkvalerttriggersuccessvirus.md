#### Parser Content
```Java
{
Name = "fortinet-utm-kv-alert-trigger-success-virus"
Vendor = "Fortinet"
Product = "Fortinet UTM"
TimeFormat = "yyyy-MM-dd' time='HH:mm:ss"
Conditions = [
  """subtype="""
  """virus="""
  """action="""
  """dtype="Virus""""
]
Fields = [
  """date=({time}\d\d\d\d-\d\d-\d\d time\=\d\d:\d\d:\d\d)"""
  """\Wdevname="*({host}[^\s"]+)"*(\s|")"""
  """\Wsrcip="*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Wdstip="*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\Wvirus="*({alert_name}.+?)["\s]*(\w+=|$)"""
  """\Wdtype="*({alert_type}.+?)["\s]*(\w+=|$)"""
  """\Wvirusid=({alert_id}\d+)(\s|")"""
  """\Wurl="*({malware_url}[^"\s]+)"""
  """\Wref="*({additional_info}[^"\s]+)"""
  """\Wuser="*({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """\Wcrlevel=({alert_severity}[^"\s]+)(\s|")"""
  """\Wsrcport=({src_port}\d+)"""
  """\Wdstport=({dest_port}\d+)"""
  """\Wservice="({protocol}[^"]+)""""
  """\Wfilename="({malware_file_name}[^"]+)""""
  """\Waction="({action}[^"]+)"""",
  """\Wtz="?({tz}[+-]\d+)"""
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
    "src_ip->malwareVictimHost"
    "malware_url->malwareAttackerUrl"
    "alert_type->description"
    "dest_ip->malwareAttackerIp"
    "malware_url->process_name"
  ]
  NameTemplate = "Fortinet Alert ${alert_name} found"
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