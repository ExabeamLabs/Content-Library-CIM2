#### Parser Content
```Java
{
Name = pan-wildfire-leef-alert-trigger-success-threat
  Vendor = Palo Alto Networks
  Product = Palo Alto WildFire
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = ["""LEEF:1.0|Palo Alto Networks""", """cat=THREAT|subtype=wildfire""" ]
  Fields = [
    """\s({host}[\w\.-]+)\s+LEEF:""",
    """subtype=({alert_type}wildfire)""",
    """Severity=({alert_severity}\d+)""",
    """Severity=({alert_severity}[^\|]+)\|""",
    """(URLCategory|Severity)=({alert_severity}benign|informational)""",
    """usrName =(({domain}[^\\]+)\\)?(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\|(SerialNumber|SourceUser)""",
    """DestinationUser=(?:[^\\/]+[\\/])?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\|Application=""",
    """\|src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\|dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\|""",
    """SessionID=({alert_id}[^|]+)\|""",
    """LEEF[^|]+?\|([^\|]+\|){3}({alert_name}[^|]+)\|""",
    """\|URLCategory=({category}[^\|]*)\|""",
    """\|Miscellaneous="?({miscellaneous}[^\|"]+)"?\|"""
  ]
  DupFields = [ "miscellaneous->malware_url" ]
  SOAR {
    IncidentType = "malware"
    DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "alert_name->malwareName", "category->malwareCategory", "alert_severity->sourceSeverity", "src_ip->malwareVictimHost", "alert_type->description", "malware_url->malwareAttackerUrl", "dest_ip->malwareAttackerIp"]
    NameTemplate = """Palo Alto Alert ${alert_name} found"""
    ProjectName = "SOC"
    EntityFields = [
      {EntityType="device", Name ="src_address", Fields=["src_ip->ip_address"]

}
```