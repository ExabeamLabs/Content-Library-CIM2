#### Parser Content
```Java
{
Name = mcafee-es-json-alert-trigger-success-avdetect
  ExtractionType = json
  ParserVersion = v1.0.0
  Vendor = McAfee
  Product = McAfee Endpoint Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"analyzername":"""", """"threatcategory":"av.detect"""", """"mccomputername":"""" ]
  Fields = [
    """exa_json_path=$.generatedtime,exa_field_name=time""",
    """exa_json_path=$.targetusername,exa_regex=^(({domain}[^"\\]+)\\+)?({user}[\w\.\-]{1,40}\$?)$""",
    """exa_json_path=$.domainname,exa_field_name=domain""",
    """exa_json_path=$.ipaddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.threatcategory,exa_field_name=({threat_category}[^"]+)""",
    """exa_json_path=$.threatactiontaken,exa_field_name=action""",
    """exa_json_path=$.sourceprocessname,exa_regex=({process_path}(({process_dir}[^"]+?)\\+)?({process_name}[^"\\]*))$""",
    """exa_json_path=$.operatingsystem,exa_field_name=os""",
    """exa_json_path=$.analyzerdetectionmethod,exa_regex=(\s+|({additional_info}[^"]+))""",
    """exa_json_path=$.action,exa_field_name=alert_name""",
    """exa_json_path=$.autoid,exa_field_name=alert_id""",
    """exa_json_path=$.targetfilename,exa_regex=^({malware_url}.*?[\\\/]?({malware_file_name}[^\\\/]+?))$""",
    """exa_json_path=$.analyzername,exa_field_name=event_name""",
    """exa_json_path=$.threattype,exa_field_name=alert_type""",
    """exa_json_path=$.mccomputername,exa_field_name=src_host""",
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