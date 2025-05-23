#### Parser Content
```Java
{
Name = "mcafee-es-kv-alert-trigger-success-timestamp"
Vendor = "Trellix"
Product = "Trellix Endpoint Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """_timestamp="""
  """signature_id"""
  """threat_handled"""
  """is_laptop"""
]
Fields = [
  """detected_timestamp="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
      """signature="({alert_name}[^"]+)"""",
      """signature_id="({signature_id}[^"]+)"""",
      """category="({threat_category}[^"]+)"""",
      """AnalyzerHostName ="({host}[^"]+)"""",
      """severity_id="({alert_severity}\d+)"""",
      """SourceIPV4="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """TargetIPV4="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
      """threat_type="({alert_type}[^"]+)"""",
      """file_name="*(\s*|({malware_url}[^"]+?))"""",
      """ Name ="({additional_info}[^"]+)"""",
      """domain_name="({domain}[^"]+)"""",
      """user_name="*(N\/A|\s+|NULL|([^\\]+\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
      """AutoID="({alert_id}[^"]+)"""",
      """TargetProcessName ="({process_name}[^"]+)"""",
      """target_process_parent_name="({parent_process_name}[^"]+)"""",

]
SOAR {
  IncidentType = "malware"
  DupFields = [
    "time->startedDate"
    "vendor->source"
    "rawLog->sourceInfo"
    "alert_id->sourceId"
    "alert_name->malwareName"
    "alert_type->malwareCategory"
    "alert_severity->sourceSeverity"
    "src_host->malwareVictimHost"
    "malware_url->malwareAttackerFile"
  ]
  NameTemplate = "McAfee EPO Alert ${alert_name} found"
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