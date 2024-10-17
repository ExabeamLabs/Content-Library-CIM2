#### Parser Content
```Java
{
Name = sentinelone-singularityp-cef-alert-trigger-success-classification
  ParserVersion = v1.0.0
  Vendor = SentinelOne
  Product = Singularity Platform
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """"classification":""", """"threatName":"""", """"mitigationStatus":""", """"engines":"""]
  Fields = [
     """CEF:([^\|]*\|){5}({alert_name}[^\|]+)\|({alert_severity}[^\|]+)\|"""
     """"createdAt":\s*"({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)""",
     """"updatedAt":\s*"({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)""",
     """"title":\s*"({alert_name}[^"]+)""",
     """"classification":\s*"({alert_name}({alert_type}[^"]+))""",
     """"agentIp(V4|V6)?":\s*"(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
     """"fileDisplayName":\s*"({file_name}[^"]+)""",
     """"filePath":\s*"({file_path}[^"]+)""", 
     """"agentDomain":\s*"(unknown|({src_domain}[^"]+))""",
     """"agentComputerName":\s*"({src_host}[^"]+)""",
     """"fileExtensionType":(\s*"None|null|\s*"+(Unknown|({file_type}[^"]+))")""",
     """"agentLastLoggedInUserName":"({last_loggedin_user}[^"]+)"""",
     """"processUser":"(({domain}[^\\"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)",""",
     """\Wsuser=(({domain}[^\\\/=]+)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+\w+=|\s*$)""",
     """"username":"(({domain}[^\\"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)",""",
     """"rank":({alert_severity}\d+)""",
     """"mitigationReport":({additional_info}\{.{1,400}?\}\}),""",
     """"fileContentHash":"({hash_md5}[^"]+)"""",
     """"id":"({alert_id}\d+)"""",
     """"action":"({action}quarantine)".*?"status":"({quarantine_status}\w+)"""",
     """"action":"({action}kill)".*?"status":"({kill_status}\w+)"""",
     """"mitigationStatus":"({result}[^"]+)"""",
     """"threatId":"({alert_id}\d+)"""",
     """"agentDetectionInfo".*?"siteName":"({site_name}[^"]+)"""",
     """"threatInfo".*?"originatorProcess":"({src_process_name}[^"]+)"""",
     """"agentDetectionInfo".*?"agentMitigationMode":"({mitigation_mode}[^"]+)"""",
     """"mitigationMode":"({mitigation_mode}[^"]+)"""",
     """"agentMachineType":"({host_type}[^"]+)"""",
     """"agentOsType":"({os}[^"]+)"""",
     """"incidentStatus":"({incident_status}[^"]+)"""",
     """"analystVerdict":"({verdict}[^"]+)"""",
     """"groupName":"({group_name}[^"]+)"""",
     """({alert_source}SentinelOne)""",
     """msg=.*?Alert Detected by\s*\[({alert_source}[^\]]+)\]""",
     """"confidenceLevel":"({category}[^"]+)""",
     """"filePath":\s*"([^"\(\)]+[\\\/]+?)?({malware_file_name}[^"]+)"""",
     """"sha1":"({hash_sha1}[^",]+)""",
     """"externalIp":\s*\"({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_translated_port}\d+))?"""",
     """"fileSize":({bytes}\d+)"""
  ]
   SOAR {
    IncidentType = "malware"
    DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "alert_name->malwareName", "src_host->malwareVictimHost", "alert_type->description", "malware_url->malwareAttackerUrl","file_name->malwareAttackerFile"]
    NameTemplate = """SentinelOne Alert ${alert_name} found"""
    ProjectName = "SOC"
    EntityFields = [
      {EntityType="device", Name ="src_address", Fields=["src_ip->ip_address", "src_host->host_name"]

}
```