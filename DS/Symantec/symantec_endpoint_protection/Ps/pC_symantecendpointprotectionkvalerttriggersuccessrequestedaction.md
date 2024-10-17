#### Parser Content
```Java
{
Name = symantec-endpointprotection-kv-alert-trigger-success-requestedaction
  Vendor = Symantec
  Product = Symantec Endpoint Protection
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """,Actual action:""",""",Requested action:""" ]
  Fields = [
			"""Computer name:\s*(?:0+|({host}[^,]+))"""
			"""Event time:\s*({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""
			"""Risk name:\s*({alert_name}({alert_type}[^,]+)),"""
			"""Risk type:\s*({alert_type}[^,]+),"""
			"""({alert_type}Virus found)"""
			"""IP Address:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
			"""\d\d:\d\d:\d\d,\s*({alert_severity}Minor|Info|Critical|Major|Security risk found|Virus found)"""
			"""Sensitivity:\s({alert_severity}[^,]+)"""
			"""Risk Level:\s*(N\/A|({alert_severity}[^,]+))"""
			"""Occurrences:\s*\d+,(File path:\s+)?({malware_url}[^,]+)"""
			"""User\s*(Name)?:\s*(SYSTEM,|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
			"""Computer name:\s*(?:0+|({src_host}[^,]+))"""
			"""Source computer:\s*(?:0+|({dest_host}[^,]+))?,"""
			"""Source IP:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
			"""Confidence:\s*({additional_info}[^,]+)"""
			"""Actual action:\s*({action}[^,]+)"""
			"""Application hash:\s*(|({file_hash}[^,]+)),"""
			"""Hash type:\s*(|({hash_type}[^,]+)),"""
			"""Application name:\s\"*({process_name}[^\",]+)"""
			"""File size \(bytes\):\s*({bytes}\d+)"""
        ]
  SOAR {
    IncidentType = "malware"
    DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "alert_name->malwareName", "alert_type->malwareCategory", "src_host->malwareVictimHost", "malware_url->malwareAttackerFile", "dest_ip->malwareAttackerIp"]
    NameTemplate = """Symantec Alert ${alert_name} found"""
    ProjectName = "SOC"
    EntityFields = [
      {EntityType="device", Name ="src_address", Fields=["src_ip->ip_address", "src_host->host_name"]

}
```