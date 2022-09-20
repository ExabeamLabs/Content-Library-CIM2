#### Parser Content
```Java
{
Name = mcafee-es-kv-alert-trigger-success-367
  ParserVersion = v1.0.0
  Vendor = McAfee
  Product = McAfee Endpoint Security
  TimeFormat = "epoch"
  Conditions = [ """|McAfee|ESM|""", """|367-""" ]
  Fields = [ """\send=({time}\d+).*\snitroThreat_Category=(?!ops\.task\.cancel|hip\.file|None)""",
    """\sdeviceTranslatedAddress=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\ssrc=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\sshost=({src_host}[^\s]+)""",
    """\|McAfee\|ESM\|[^\|]+\|367-({signature_id}[^\|]+)\|({alert_type}[^\|]+).*?\seventId=({alert_id}[^\s]+).*\snitroThreat_Name =({alert_name}.+?)\s[^\s]+?=""",
    """\sduser=([^\\=]+?\\)?({user}.+?)\s[^\s]+?=""",
    """\sdst=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\snitroDestination_Filename=({url}.+?\\+({malware_file_name}[^\\]+?))\s[^\s]+?="""
  ] 
  SOAR {
    IncidentType = "malware"
    DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "alert_id->sourceId", "alert_name->malwareName", "src_host->malwareVictimHost", "url->malwareAttackerUrl", "alert_type->malwareCategory", "malware_file_name->malwareAttackerFile", "dest_ip->malwareAttackerIp"]
    NameTemplate = """McAfee EPO Alert ${alert_name} found"""
    ProjectName = "SOC"
    EntityFields = [
      {EntityType="device", Name ="src_address", Fields=["src_ip->ip_address", "src_host->host_name"]

}
```