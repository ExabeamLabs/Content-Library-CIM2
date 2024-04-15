#### Parser Content
```Java
{
Name = "fireeye-networksecurity-csv-alert-trigger-success-webmps"
Vendor = "FireEye"
Product = "FireEye Web MPS"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""CSV:0:FireEye:Web MPS"""
]
Fields = [
""",occurred=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
"""dvchost=({host}[^,]+)"""
"""alertid=({alert_id}\d+)"""
"""alertType=({alert_type}[^,]+)"""
"""alertType=({alert_name}[^,]+)"""
"""sev=({alert_severity}[^,]+)"""
"""sname=({alert_name}[^,]+)"""
"""src=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""shost=({src_host}[^,]+)"""
"""cnchost=(({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[^,]+))"""
"""dst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""dhost=({dest_host}[^,]+)"""
"""~+User-Agent:\s+({user_agent}.+?)::"""
"""mwurl=({malware_url}[^,]+)"""
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
"src_ip->malwareVictimHost"
"malware_url->malwareAttackerUrl"
"dest_ip->malwareAttackerIp"
  ]
  NameTemplate = "FireEye Alert ${alert_name} found"
  ProjectName = "SOC"
  EntityFields = [
    {
      EntityType = "device"
      Name = "src_address"
      Fields = [
"""src_ip->ip_address"""
"""src_host->host_name"""
      ]
    

}
```