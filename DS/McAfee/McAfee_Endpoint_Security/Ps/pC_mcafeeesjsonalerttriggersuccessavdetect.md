#### Parser Content
```Java
{
Name = mcafee-es-json-alert-trigger-success-avdetect
  ParserVersion = v1.0.0
  Vendor = McAfee
  Product = McAfee Endpoint Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"analyzername":"""", """"threatcategory":"av.detect"""", """"mccomputername":"""" ]
  Fields = [
    """"generatedtime":"({time}[^"]+)"""",
    """"targetusername":"(({domain}[^"\\]+)\\+)?({user}[^"\\\s]+)"""",
    """"domainname":"({domain}[^"]+)"""",
    """"ipaddress":"({src_ip}[^"]+)"""",
    """"threatcategory":"({threat_category}[^"]+)"""",
    """"sourceprocessname":"({process_path}(({process_dir}[^"]+?)\\+)?({process_name}[^"\\]*))"""",
    """"operatingsystem":"({os}[^"]+)"""",
    """"analyzerdetectionmethod":"(\s+|({additional_info}[^"]+))"""",
    """"action":"(_|({alert_name}[^"]+))"""",
    """"autoid":({alert_id}[^",]+)""",
    """"targetfilename":"({url}.*?[\\\/]?({malware_file_name}[^\\\/]+?))"""",
    """"analyzername":"({event_name}[^"]+)"""",
    """"threattype":"(\s+|({alert_type}[^"]+))"""",
    """"mccomputername":"({src_host}[^"]+)"""",
  ]
  SOAR {
    IncidentType = "malware"
    DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "alert_name->malwareName", "threat_category->malwareCategory", "alert_id->sourceId", "src_host->malwareVictimHost", "malware_file_name->malwareAttackerFile", "alert_type->malwareCategory", "url->malwareAttackerUrl"]
    NameTemplate = """Mcafee Alert ${alert_name} found"""
    ProjectName = "SOC"
    EntityFields = [
      {EntityType="device", Name ="src_address", Fields=["src_ip->ip_address", "src_host->host_name"]

}
```