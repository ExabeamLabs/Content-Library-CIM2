#### Parser Content
```Java
{
Name = mcafee-es-sk4-alert-trigger-success-analyzername
  ParserVersion = v1.0.0
  Vendor = McAfee
  Product = McAfee Endpoint Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"name":"threatcategory"""", """"name":"threatname"""", """"name":"analyzername"""" ]
  Fields = [
    """"receivedutc":\{[^\}]+?"value":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,3})?Z)"""",
    """"analyzerhostname":\{[^\}]+?"value":"({host}[^"]+)"""",
    """"sourceipv6":\{[^\}]+?"value":"\/?({src_ip}[a-fA-F\d:.]+)"""",
    """"sourceipv4":\{[^\}]+?"value":"({src_ip}[a-fA-F\d:.]+)"""",
    """"threatseverity":\{[^\}]+?"value":({alert_severity}\d{1,5})\}""",
    """"threatactiontaken":\{[^\}]+?"value":"(none|({action}[^"]+))"""",
    """"threatname":\{[^\}]+?"value":"(\_|({alert_name}[^"]+))"""",
    """"threattype":\{[^\}]+?"value":"( |({alert_type}[^"]+))"""",
    """"threateventid":\{[^\}]+?"value":({alert_id}\d+)""",
    """"threatcategory":\{[^\}]+?"value":"({threat_category}[^"]+)"""",
    """"targetusername":\{[^\}]+?"value":"((NT SERVICE|({domain}[^"\\]+))\\+)?({user}[^"]+)"""",
    """"sourceusername":\{[^\}]+?"value":"((NT SERVICE|({domain}[^"\\]+))\\+)?({user}[^"]+)"""",
    """"targetprocessname":\{[^\}]+?"value":"(null|({auth_process}(({process_dir}[^"]*?)\/+)?({process_name}[^"\/]+)))"""",
    """"targethostname":\{[^\}]+?"value":"({src_host}[^"]+)"""",
    """"analyzerdetectionmethod":\{[^\}]+?"value":"({additional_info}[^"]+)"""",
    """"targetfilename":\{[^\}]+?"value":"(?:|null|({malware_url}[^"]+?[\\\/]?({malware_file_name}[^\\\/"]+?)))""""
  ]
  SOAR {
    IncidentType = "malware"
    DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "alert_name->malwareName", "threat_category->malwareCategory", "alert_severity->sourceSeverity", "alert_id->sourceId", "src_host->malwareVictimHost", "malware_file_name->malwareAttackerFile", "alert_type->malwareCategory", "action->description"]
    NameTemplate = """Mcafee Alert ${alert_name} found"""
    ProjectName = "SOC"
    EntityFields = [
      {EntityType="device", Name ="src_address", Fields=["src_host->host_name"]

}
```