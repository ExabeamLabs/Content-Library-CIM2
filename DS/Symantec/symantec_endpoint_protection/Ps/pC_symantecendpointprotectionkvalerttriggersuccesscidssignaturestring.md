#### Parser Content
```Java
{
Name = symantec-endpointprotection-kv-alert-trigger-success-cidssignaturestring
Vendor = "Symantec"
Product = "Symantec Endpoint Protection"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""CIDS Signature string"""
"""Intrusion ID:"""
]
Fields = [
"""Local:\s*({dest_ip}[a-fA-F:\.\d]+),(Local:\s*(?:0+|({dest_host}[^,]+)))?.*?,Inbound,"""
"""Remote:\s*({src_ip}[a-fA-F:\.\d]+),(Remote:\s*(?:0+|({src_host}[^,]+)))?.*?,Inbound,"""
"""Local:\s*({src_ip}[a-fA-F:\.\d]+),(Local:\s*(?:0+|({src_host}[^,]+)))?.*?,Outbound,"""
"""Remote:\s*({dest_ip}[a-fA-F:\.\d]+),(Remote:\s*(?:0+|({dest_host}[^,]+)))?.*?,Outbound,"""
"""Remote Host Name:\s*(|({src_host}[\w\-.]+)),(Remote Host IP:\s*(?:0+|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?),)?.*?,Inbound,"""
"""Remote Host Name:\s*(|({dest_host}[\w\-.]+)),(Remote Host IP:\s*(?:0+|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?),)?.*?,Outbound,"""
"""Local Host IP:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?.*?,Outbound,"""
"""Local Host IP:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?.*?,Inbound,"""
"""Begin:\s*({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)"""
"""User( Name)?:\s*(({full_name}[^,\s]+(\s+[^,\s]+)+)|(none|({user}[^,]+))),"""
"""Domain:(?:\s+|\s*({domain}[^,]+)),"""
"""Application:(?:\s+|\s*({process_path}({process_dir}(?:[^,]+)?[\\\/])?({process_name}[^\\\/,]+?))),"""
"""CIDS Signature ID:\s*({alert_name}\d+),"""
"""Intrusion ID:\s*({alert_id}\d+),"""
"""CIDS Signature string:\s*(|({alert_type}[^:,]+?))\s*,"""
"""CIDS Signature string:\s*(|({alert_name}[^:,]+)),"""
"""CIDS Signature string:\s*({alert_type}[^:,]+?)\s*:\s*({alert_name}[^,]+)"""
"""Intrusion URL:(?:\s+|\s*({malware_url}[^,]+)),"""
"""CIDS Signature ID:\s*({alert_id}\d+),"""
"""\d\d:\d\d:\d\d,\s*({alert_severity}Minor|Info|Critical|Major|Security risk found|Virus found)"""
"""Attack:\s*({additional_info}[^\.:]+)"""
"""\w{3}\s+\d{1,2}\s\d{1,2}:\d{1,2}:\d{1,2}\s({host}[\w\.-]+)\s"""
"""({host}[^\s,]+),SHA-256:"""
]
SOAR {
  IncidentType = "malware"
  DupFields = [
"time->startedDate"
"vendor->source"
"rawLog->sourceInfo"
"alert_name->malwareName"
"alert_id->sourceId"
"src_ip->malwareVictimHost"
"malware_url->malwareAttackerUrl"
"dest_ip->malwareAttackerIp"
  ]    
  NameTemplate = "Symantec Alert ${alert_name} found"
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