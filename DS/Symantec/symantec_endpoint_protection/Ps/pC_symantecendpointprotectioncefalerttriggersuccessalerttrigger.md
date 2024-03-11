#### Parser Content
```Java
{
Name = symantec-endpointprotection-cef-alert-trigger-success-alerttrigger
  ParserVersion = v1.0.0
  Product = Symantec Endpoint Protection
  Conditions = ["""|Symantec|Endpoint Protection|"""]
  Fields = ${SymantecParsersTemplates.symantec-epp-cef-alert-1.Fields} [
    """\scatdt=({category}[^=]+?)\s+(\w+=|$)""",
    """\scs6=({category}[^=]+?)\s+(\w+=|$)""",
    """\scn1=({viruses_num}\d+)""",
  ]
  SOAR {
    IncidentType = "malware"
      DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "alert_name->malwareName", "alert_severity->sourceSeverity", "alert_id->sourceId", "src_host->malwareVictimHost", "alert_type->description", "malware_url->malwareAttackerUrl"]
      NameTemplate = """Symantec Alert ${alert_name} found"""
      ProjectName = "SOC"
      EntityFields = [
        {EntityType="device", Name ="src_address", Fields=["src_ip->ip_address", "src_host->host_name"]
symantec-epp-cef-alert-1 = {
  Vendor = Symantec
  TimeFormat = "epoch"
  Fields = [
    """\srt=({time}\d{13})""",
    """\scs1=({alert_name}[^=]+?)\s+(\w+=|$)""",
    """\sduser=((?i)(system|none)|({user}[^=]+?))\s+(\w+=|$)""",
    """\ssuser=((?i)(system|none)|({user}[^=]+?))\s+(\w+=|$)""",
    """\sfname=\w:\\+[uU]sers\\+({user}[^\\]+)""",
    """\sfname=[\s ]*({malware_file_name}[^=]+?)\s+(\w+=|$)""",
    """\seventId=({alert_id}\d+)""",
    """\sdvc=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\sahost=({host}[^\s]+)""",
    """\sdvchost=({host}[^\s]+)""",
    """\sdhost=({src_host}[^\s]+)""",
    """\sdst=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\|Symantec\|Endpoint Protection\|([^|]*?\|){2}({alert_type}[^|(]+?)\s*(\([^|]*?)?\|(Unknown|({alert_severity}[^|]+))\|""",
    """\scat=({scan_type}[^=]+?)\s+(\w+=|$)""",
    """\sfilePath=({malware_url}[^=]+?)\s+\w+=""",
    """\sfileHash=({hash_md5}[^\s]+)""",
    """\scs2=({result}[^=]+?)\s+(\w+=|$)""",
    """\scs3=({secondary_action}[^=]+?)\s+(\w+=|$)""",
    """\scs5=((?i)(\(Unknown\) \[-1\])|({process_name}[^=]+?))\s+(\w+=|$)""",
  ]
  DupFields = [ "alert_type->protection_name" 
}
```