#### Parser Content
```Java
{
Name = "fireeye-networksecurity-xml-alert-trigger-success-msgnormal"
 ParserVersion = "v1.0.0"
 Vendor = "Trellix"
 Product = "Trellix Web MPS"
 TimeFormat = "yyyy-MM-dd HH:mm:ss"
 Conditions = [
   """msg="normal"""
   """product="Web MPS""""
   """<src vlan="""
 ]
 Fields = [
   """<occurred>({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
   """ fenotify-({alert_id}\d+)"""
   """<alert id="({alert_id}[^"]+)"""
   """<src vlan=".+">\s*<ip>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
   """<src .+?<host>({src_host}[^<]+)"""
   """xsi:schemaLocation=.+?name="({alert_type}[^"]+)".*severity="({alert_severity}[^"]+)""""
   """<malware name="({alert_name}[^"]+)""""
   """<dst>.+?<ip>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?</ip"""
 ]
 SOAR {
   IncidentType = "malware"
  DupFields = [
    "time->startedDate"
     "vendor->source"
     "rawLog->sourceInfo"
     "alert_name->malwareName"
     "alert_id->sourceId"
     "alert_type->malwareCategory"
     "alert_severity->sourceSeverity"
     "src_host->malwareVictimHost"
     "dest_ip->malwareAttackerIp"
  ]
   NameTemplate = "FireEye Alert ${alert_name} found"
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