#### Parser Content
```Java
{
Name = symantec-dlp-kv-email-send-vontu
Vendor = "Symantec"
Product = "Symantec DLP"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """type=Vontu_"""
  """|lanid="""
  """|rules="""
]
Fields = [
  """\d\d:\d\d:\d\d\s+({host}[^\s]+)\s+type="""
  """\|incidentID=({alert_id}\d+)"""
  """\|policy=({alert_name}[^|]+)\|"""
  """\|rules=({alert_type}[^|]+)\|"""
  """\|(src|suser)=(?:({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|((?!\w+[:@]+))({src_host}[^|\s]+))"""
  """\|(src|suser)=(?=[^\s@]+@(?!\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))({src_email_address}[^|\s]+)"""
  """\|(src|suser)=({user}[^@|]+)@[^|]+"""
  """\|subject=(?:N\/A|({email_subject}[^|]+))"""
  """\|subject=(?=\s*FTP\s*)\s*({protocol}FTP)\s*({file_name}[^|]+)"""
  """\|(dst|duser)=(?:N\/A|({target}[^|]+))"""
  """\|(dst|duser)=(?=\w+:\/)({protocol}.+?):\/+"""
  """\|(dst|duser)=({account}[^@]+)@({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(:({dest_port}\d+))?"""
  """\|(dst|duser)=(?=[^\s@]+@(?!\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))({email_recipients}[^|]+)"""
  """\|(dst|duser)=(?=[^\s@]+@(?!\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))({dest_email_address}[^|,]+)"""
  """\|endpoint=(?:N\/A|({src_host}[^$|\s]+))"""
  """\|fileName =(?:N\/A|({file_name}[^|]+))"""
  """\|fileName =(?=http(s)?:)({protocol}[^:|]+)"""
  """\stype=({additional_info}[^|]+)"""
  """\|blocked=({action}[^|]+)"""
]
SOAR {
  IncidentType = "dlp"
  DupFields = [
    "time->startedDate"
    "vendor->source"
    "rawLog->sourceInfo"
    "user->dlpUser"
    "alert_name->dlpPolicy"
    "protocol->dlpProtocol"
    "src_host->dlpDeviceName"
    "file_name->dlpFileName"
    "action->dlpActionTaken"
  ]
  NameTemplate = "Symantec DLP Alert ${alert_name} found"
  ProjectName = "SOC"
  EntityFields = [
    {
      EntityType = "device"
      Name = "src_address"
      Fields = [
        """src_ip->ip_address"""
        """src_host->host_name"""
      ]
    

}
```