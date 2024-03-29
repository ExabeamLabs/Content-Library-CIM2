#### Parser Content
```Java
{
Name = symantec-dlp-leef-alert-email-modified
Vendor = "Symantec"
Product = "Symantec DLP"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """LEEF:"""
  """|Symantec|DLP|"""
  """|subject="""
]
Fields = [
  """\s({host}[\w.\-]+)\s+LEEF:"""
  """\|incidentID=({alert_id}\d+)"""
  """\|Symantec\|DLP\|({alert_severity}[^\|]+)\|"""
  """\|Symantec\|DLP\|[^|]+?\|({alert_name}[^|]+?)\s*\|"""
  """\|usrName =(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({email_address}[^\|@]+@[^\|@]+)|(N/A|({user}[^\|]+)))"""
  """\|suser=((NT AUTHORITY|({domain}[^\|\\\/]+))[\\\/]+)?(system|N/A|({user}[^\|\\\/]+))\|"""
  """\|usrName =(N/A|({user}[^\|@]+))@"""
  """\|usrName =(?=[\w.]+@[\w.])({src_email_address}[^\|]+)"""
  """\|duser=(?=[\w.]+@[\w.])({email_recipients}[^\|]+)"""
  """\|subject=\s*((?!SFTP|HTTP|FTP|TCP|N/A)({email_subject}[^\|]+?))\s*\|"""
  """\|rules=\s*({alert_type}[^\|]+?)\s*\|"""
  """\|duser=({account}.+?)@({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\|[^|]+?\|subject=({protocol}FTP)"""
  """\|subject=FTP\s+({file_name}.+?)\s+\(({bytes}\d+)\s+({bytes_unit}[^\)]+)"""
  """\|duser=({target}[^\|]+)\|[^|]+?\|subject=({protocol}HTTP)"""
  """\|incidentSnapshot=((?!\d{1,3}\.\d{1,3}\.\d{1,3})({url}(\w+:\/+)?({web_domain}[^\\\/]+)[^\s]+))\s+(\w+=|$)"""
  """\|subject=({protocol}TCP:Pop3|SFTP)\|"""
  """\|Protocol=.+?({protocol}SMTP|FTP|HTTP|HTTPS)\|"""
  """\|fileName =(N\/A|({file_name}[^\|]+))"""
  """\|parentPath=(N\/A|({file_path}[^\|]+))"""
  """\|blocked=(None|({action}[^\|]+?))\s*\|"""
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
    "src_ip->dlpDeviceName"
    "file_name->dlpFileName"
    "action->dlpActionTaken"
    "email_subject->emailSubject"
    "src_email_address->emailFrom"
    "email_recipients->emailTo"
  ]
  NameTemplate = "Symantec DLP Alert ${alert_name} found"
  ProjectName = "SOC"
  EntityFields = [
    {
      EntityType = "device"
      Name = "src_address"
      Fields = [
        """src_ip->ip_address"""
      ]
    

}
```