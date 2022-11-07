#### Parser Content
```Java
{
Name = symantec-dlp-kv-email-send-incident-1
Vendor = "Symantec"
Product = "Symantec DLP"
TimeFormat = "MMM dd, yyyy HH:mm:ss a"
Conditions = [
  """Symantec|DLP|"""
  """|policy="""
  """|incidentSnapshot="""
]
Fields = [
  """\|occurredon=({time}\w+ \d+, \d+ \d+:\d+:\d+ \w+)\|"""
  """({host}[\w.\-]+)\s+Symantec\|DLP\|"""
  """\|severity=({alert_severity}[^\|]+)"""
  """\|policy=({alert_name}[^\|]+)"""
  """\|policy=([^-\|]*\-)?\s*({alert_type}[^\|]+)"""
  """\|rules=({rule}[^\|]+)"""
  """\|action=(None|({action}[^\|]+))"""
  """\|incidentID=({alert_id}\d+)"""
  """\|protocol=({protocol}[^\|]+?)\s*(\||$)"""
  """\|subject=((?!SFTP|HTTP|FTP|TCP|N\/A)({email_subject}[^\|]+))"""
  """\|fileName =(?!https:|N\/A).*?({file_name}[^\|]+)"""
  """\|AttachmentName =(N\/A|({file_name}[^\|]+?))\s*(\||$)"""
  """\|endpointusrname=(N\/A|(({domain}[^\\]+)\\+)?({user}[^\s\|]+))"""
  """\|Username=(N\/A|(({domain}[^\\\|]+)\\+)?({user}[^\s\|]+))"""
  """\|subject.*?\|Username=(N\/A|(({domain}[^\\]+)\\+)?({user}[^\s\|]+))"""
  """\|(Username|src)=({user}[^\s@\|]+@[^@\s\|]+)"""
  """\|(Username|src)=WinNT:\/+({domain}[^\\\/\|]+)(\\|\/)+({user}[^\s\|]+)"""
  """\|endpointhostname=(N\/A|({src_host}[\w\-.]+))"""
  """\|endpointipaddress=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\|sender=(?=[\w.]+@[\w.])({email_address}[^\|]+)"""
  """\|sender=(?=[\w.]+@[\w.])({user}[^\|]+)"""
  """\|EmailAddress=({email_address}[^\|]+?)\s*(\||$)"""
  """\|recipients=({target}[^\|]+?)\s*(\||$)"""
  """\|destination=({target}[^\|]+?)\s*(\||$)"""
  """\|incidentSnapshot=\w+:\/+[^\s]*?((?!\d{1,3}\.\d{1,3}\.\d{1,3})({url}[^\s]+))\s*(\||$)"""
  """\|matchCount=({match_count}[^\|]+?)\s*(\||$)"""
]
DupFields = [
  "protocol->alert_type"
]
SOAR {
  IncidentType = "dlp"
  DupFields = [
    "time->startedDate"
    "vendor->source"
    "rawLog->sourceInfo"
    "user->dlpUser"
    "alert_name->dlpPolicy"
    "alert_severity->sourceSeverity"
    "protocol->dlpProtocol"
    "file_name->dlpFileName"
    "action->dlpActionTaken"
  ]
  NameTemplate = "Symantec DLP Alert ${alert_name} found"
  ProjectName = "SOC"
  EntityFields = [
    {
      EntityType = "device"
      Name = "dest_address"
      Fields = [
        """dest_ip->ip_address"""
        """dest_host->host_name"""
      ]
    

}
```