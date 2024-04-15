#### Parser Content
```Java
{
Name = "fortinet-utm-kv-alert-trigger-success-ips"
Vendor = "Fortinet"
Product = "Fortinet UTM"
TimeFormat = "yyyy-MM-dd' time='HH:mm:ss"
Conditions = [
  """subtype=ips"""
  """action=detected"""
  """service="""
  """date="""
]
Fields = [
  """\Wdate=({time}\d\d\d\d-\d\d-\d\d time\=\d\d:\d\d:\d\d)"""
  """\Wdevname="?({host}[^"]+?)"?(\s+\w+=|\s*$)"""
  """\Wprofile="({alert_type}[^"]+)""""
  """\Wsrcip=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Wdstip=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\Wseverity="?({alert_severity}\w+)"""
  """\Wsrcport=({src_port}\d+)"""
  """\Wdstport=({dest_port}\d+)"""
  """\Wservice="?({protocol}\w+)"""
  """\Wattack="({alert_name}[^"]+)""""
  """\Wmsg="({additional_info}[^"]+)""""
  """\Waction="?({action}[^"]+?)"?(\s+\w+=|\s*$)"""
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