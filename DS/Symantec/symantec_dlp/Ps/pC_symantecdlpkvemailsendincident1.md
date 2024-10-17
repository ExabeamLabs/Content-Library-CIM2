#### Parser Content
```Java
{
Name = symantec-dlp-kv-email-send-incident-1
Vendor = "Symantec"
Product = "Symantec DLP"
TimeFormat = ["MMM dd, yyyy hh:mm:ss a","MMM dd HH:mm:ss"]
Conditions = [
  """Symantec|DLP|"""
  """|policy="""
  """|incidentSnapshot="""
]
Fields = [
  """({time}\w+\s\d+\s\d+:\d+:\d+)"""
  """occurredon=({time}\w+ \d+, \d+ \d+:\d+:\d+ \w+)\|"""
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
  """\|endpointusrname=(N\/A|(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """\|Username=(N\/A|(({domain}[^\\\|]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """\|subject.*?\|Username=(N\/A|(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """\|(Username|src)=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""
  """\|(Username|src)=WinNT:\/+({domain}[^\\\/\|]+)(\\|\/)+({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """\|endpointhostname=(N\/A|({src_host}[\w\-.]+))"""
  """\|endpointipaddress=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\|sender=(?=[\w.]+@[\w.])({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """\|sender=(?=[\w.]+@[\w.])(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
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