#### Parser Content
```Java
{
Name = "checkpoint-es-kv-alert-trigger-success-protection"
Vendor = "Check Point"
Product = "Check Point Endpoint Security"
TimeFormat = "epoch_sec"
Conditions = [
  """__policy_id_tag:"""
  """;Protection"""
]
Fields = [
  """date=({time}\d{10});"""
  """;Protection (Name|name):\s*({alert_name}[^;]+);"""
  """;malware_action:\s*({alert_type}[^;]+);"""
  """;file name:\s*({malware_file_name}[^;]+);"""
  """;file_type:\s*({malware_file_type}[^;]+);"""
  """;severity:\s*({alert_severity}\d)"""
  """src:\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """dst:\s*({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """dst_user_name:\s*[^(]+\(({user}[^)]+)"""
  """src_user_name:\s*[^(]+\(({user}[^)]+)"""
  """dst_user_name:\s*[^(]+\(({account}[^)]+).*src_user_name:\s*[^(]+\(({user}[^)]+)"""
  """;Protection Type:\s*({additional_info}[^;]+);"""
  """\Ws_port:\s*({src_port}\d+)"""
  """\Wservice:\s*({dest_port}\d+)"""
  """;Destination DNS Hostname:\s*({dest_host}[^;]+)"""
  """;src_machine_name:\s*({src_host}[^;]+)"""
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
    "malware_file_name->malwareAttackerFile"
    "dest_ip->malwareAttackerIp"
  ]
  NameTemplate = "Check Point Alert ${alert_name} found"
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