#### Parser Content
```Java
{
Name = vmware-carbonblack-leef-alert-trigger-success-activethreat
  ParserVersion = v1.0.0
  Vendor = VMware
  Product = Carbon Black CES
  TimeFormat = "MMM-dd-yyyy HH:mm:ss z"
  Conditions = [ """|CarbonBlack|CbDefense|""", """LEEF:""", """Active_Threat""" ]
  Fields = [
    """\sdevTime=({time}\w+\-\d{1,2}\-\d{4} \d\d:\d\d:\d\d \w+)""",
    """\sdeviceName =(({domain}[^\s\\]+)\\)?({src_host}[^\s\\]+)\s""",
    """\sinternalIpAddress=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s""",
    """\sexternalIpAddress=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s""",
    """\ssev=({alert_severity}\d+)\s""",
    """\ssummary=({additional_info}.+?)\s+groupName =""",
    """\ssignature=({alert_type}[^\s]+)""",
    """\sincidentId=({alert_id}[^\s]+)""",
    """\sapplicationName =({process_name}.+?)\s+indicatorName =""",
    """\|CarbonBlack\|CbDefense\|(.*?)\|({alert_name}.*?)\|""",
    """\semail=(({domain}[^\\]+)\\+)?({user}[^\\\s]+)"""
  ]
  SOAR {
    IncidentType = "malware"
    DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "alert_name->malwareName", "alert_type->malwareCategory", "dest_ip->malwareAttackerIp", "alert_severity->sourceSeverity", "alert_id->sourceId", "src_host->malwareVictimHost"]
    NameTemplate = """Carbon Black Alert ${alert_name} found"""
    ProjectName = "SOC"
    EntityFields = [
      {EntityType="device", Name ="src_address", Fields=["src_ip->ip_address"]

}
```