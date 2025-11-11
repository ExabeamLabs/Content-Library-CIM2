#### Parser Content
```Java
{
Name = symantec-endpointprotection-cef-alert-trigger-success-intrusiondetected
  Product = Symantec Endpoint Protection
  ParserVersion = v1.0.0
  Conditions = ["""|Symantec|Endpoint Protection|""", """|Intrusion Detected"""]
  Fields = ${SymantecParsersTemplates.symantec-epp-cef-alert-1.Fields} [
    """\|Symantec\|Endpoint Protection\|([^|]*?\|){2}({alert_name}[^|]+?)\|""",
    """\smsg=({additional_info}[^=]+?)\s+\w+=""",
    """\sact=({action}[^\s]+)""",
  ]
  SOAR {
    IncidentType = "malware"
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
    """\sduser=((?i)(system|none)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+(\w+=|$)""",
    """\ssuser=((?i)(system|none)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+(\w+=|$)""",
    """\sfname=\w:\\+[uU]sers\\+({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """\sfname=[\s ]*({malware_file_name}[^=]+?)\s+(\w+=|$)""",
    """\seventId=({alert_id}\d+)""",
    """\sdvc=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\sahost=({host}[^\s]+)""",
    """\sdvchost=({host}[^\s]+)""",
    """\sdhost=({src_host}[^\s]+)""",
    """\sdst=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\|Symantec\|Endpoint Protection\|([^|]*?\|){2}({alert_type}[^|(]+?)\s*(\([^|]*?)?\|(Unknown|({alert_severity}[^|]+))\|""",
    """\scat=({scan_type}[^=]+?)\s+(\w+=|$)""",
    """\sfilePath=({malware_url}[^=]+?)\s+\w+=""",
    """\sfileHash=(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))\s+""",
    """\scs2=({result}[^=]+?)\s+(\w+=|$)""",
    """\scs3=({secondary_action}[^=]+?)\s+(\w+=|$)""",
    """\scs5=((?i)(\(Unknown\) \[-1\])|({process_name}[^=]+?))\s+(\w+=|$)""",
    """\|Symantec\|Endpoint Protection\|([^|]*?\|){2}({protection_name}[^|(]+?)\s*(\([^|]*?)?\|(Unknown|({alert_severity}[^|]+))\|""",
  
}
```