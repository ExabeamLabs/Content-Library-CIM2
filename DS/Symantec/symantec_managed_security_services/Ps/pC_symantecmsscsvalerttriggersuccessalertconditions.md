#### Parser Content
```Java
{
Name = symantec-mss-csv-alert-trigger-success-alertconditions
  Vendor = Symantec
  Product = Symantec Managed Security Services
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """<Symantec MSS alert Conditions>""" ]
  Fields = [
    """({alert_id}\d+),"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+)",[^\,]+,"({alert_severity}[^"]+)",[^\,]+,"({alert_type}[^"]+)","({alert_name}[^"]+)","({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?",[^\n]+<Symantec MSS alert Conditions>"""
  ]
  SOAR {
    IncidentType = "malware"
    DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "alert_name->malwareName", "alert_severity->sourceSeverity", "alert_id->sourceId", "src_ip->malwareVictimHost", "alert_type->description"]
    NameTemplate = """Symantec Alert ${alert_name} found"""
    ProjectName = "SOC"
    EntityFields = [
      {EntityType="device", Name ="src_address", Fields=["src_ip->ip_address"]

}
```