#### Parser Content
```Java
{
Name = cisco-fp-kv-alert-trigger-success-impactbits
  Vendor = Cisco
  Product = Cisco Network Security
  ParserVersion = "v1.0.0" 
  TimeFormat = "epoch_sec"
  Conditions = [ """sec_zone_ingress=""","""impact_bits=""" ]
  Fields = [
    """\Wevent_sec=({time}\d{10})""",
    """\Wevent_id=({alert_id}\d+)""",
    """\W(msg|corr_rule)=\\?"?({alert_name}[^"\\=]+)\\?"?\s+\w+=""",
    """\W(class_desc|corr_policy)=\\?"?({alert_type}[^"\\=]+)\\?"?\s+\w+=""",
    """\Wpriority=({alert_severity}[^\s]+)""",
    """\Wsrc_ip=(0|0.0.0.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """\Wdest_ip=(0|0.0.0.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
    """\d\d:\d\d:\d\d\s+({host}[\w-]+)\s"""
    """\suser=\\?"*(0|No Authentication Required|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
  ]
  SOAR {
    IncidentType = "generic"
    DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "alert_name->description", "alert_severity->sourceSeverity"]
    NameTemplate = """Cisco Firesight Alert ${alert_type} found"""
    ProjectName = "SOC"
    EntityFields = [
      {EntityType="device", Name ="src_address", Fields=["src_ip->ip_address", "src_host->host_name"]

}
```