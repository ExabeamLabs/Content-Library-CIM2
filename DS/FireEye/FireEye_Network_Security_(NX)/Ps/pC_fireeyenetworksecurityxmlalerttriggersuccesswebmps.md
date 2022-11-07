#### Parser Content
```Java
{
Name = fireeye-networksecurity-xml-alert-trigger-success-webmps
  Vendor = FireEye
  Product = FireEye Network Security (NX)
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """msg="extended""","""product="Web MPS"""","""</ip>""" ]
  Fields = [
             """<occurred>({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
             """ fenotify-({alert_id}\d+)""",
             """<alert id="({alert_id}[^"]+)""",
             """<src vlan=\".+\">\s*<ip>({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
             """<src .+?<host>({src_host}[^<]+)""",
             """xsi:schemaLocation=.+?name="({alert_type}[^"]+)".*severity="({alert_severity}[^"]+)"""",
             """<malware name="({alert_name}[^"]+)"""",
             """<dst>.+?<ip>({dest_ip}[^<]+)</ip""",
        ]
  SOAR {
    IncidentType = "malware"
    DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "alert_name->malwareName", "alert_id->sourceId", "alert_type->malwareCategory", "alert_severity->sourceSeverity", "src_host->malwareVictimHost", "dest_ip->malwareAttackerIp"]
    NameTemplate = """FireEye Alert ${alert_name} found"""
    ProjectName = "SOC"
    EntityFields = [
      {EntityType="device", Name ="src_address", Fields=["src_ip->ip_address", "src_host->host_name"]

}
```