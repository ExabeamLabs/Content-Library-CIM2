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
    """"ipaddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"threatcategory":"({threat_category}[^"]+)"""",
    """"threatactiontaken\\*":\\*"({action}[^,"\\]+)""""
    """"sourceprocessname":"({process_path}(({process_dir}[^"]+?)\\+)?({process_name}[^"\\]*))"""",
    """"operatingsystem":"({os}[^"]+)"""",
    """"analyzerdetectionmethod":"(\s+|({additional_info}[^"]+))"""",
    """"action":"(_|({alert_name}[^"]+))"""",
    """"autoid":({alert_id}[^",]+)""",
    """"targetfilename":"({malware_url}.*?[\\\/]?({malware_file_name}[^\\\/]+?))"""",
    """"analyzername":"({event_name}[^"]+)"""",
    """"threattype":"(\s+|({alert_type}[^"]+))"""",
    """"mccomputername":"({src_host}[^"]+)"""",
  ]
  SOAR {
    IncidentType = "malware"
    DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "alert_name->malwareName", "threat_category->malwareCategory", "alert_id->sourceId", "src_host->malwareVictimHost", "malware_file_name->malwareAttackerFile", "alert_type->malwareCategory", "malware_url->malwareAttackerUrl"]
    NameTemplate = """Mcafee Alert ${alert_name} found"""
    ProjectName = "SOC"
    EntityFields = [
      {EntityType="device", Name ="src_address", Fields=["src_ip->ip_address", "src_host->host_name"]

}
```