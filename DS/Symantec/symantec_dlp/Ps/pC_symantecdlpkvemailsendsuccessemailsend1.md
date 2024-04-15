#### Parser Content
```Java
{
Name = "symantec-dlp-kv-email-send-success-emailsend-1"
Vendor = "Symantec"
Product = "Symantec DLP"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
Conditions = [
  """,endpoint_machine="""
  """,policy="""
  """,incident_snapshot="""
]
Fields = [
  """({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\d)\d\d\d[+-]\d\d:\d\d\s+({host}[\w\-.]+)"""
  """(?i)incident_id="*({alert_id}\d+)"""
  """(?i)policy="*({alert_name}[^",]+)("|,|\s*$)"""
  """(?i)protocol="*({protocol}[^",]+)("|,|\s*$)"""
  """(?i)recipients="*(?=[\w.]+@[\w.])({email_recipients}[^",]+)("|,|\s*$)"""
  """(?i)recipients="*(?=[\w.]+@[\w.])({external_address}[^",]+)("|,|\s*$)"""
  """(?i)recipients="*(?=\w+:\/+)({target}[^",]+)("|,|\s*$)"""
  """(?i)sender="*(?=[\w.]+@[\w.])({src_email_address}[^",]+)("|,|\s*$)"""
  """(?i)sender="*(?=[\w.]+@[\w.])({user}[^",]+)("|,|\s*$)"""
  """(?i)severity="*({alert_severity}[^",]+)("|,|\s*$)"""
  """(?i)subject="*(?:N\/A|({email_subject}[^",]+))("|,|\s*$)"""
  """\s(?i)file_name="*(?:N\/A|({file_name}[^",]+))\s*("|,|\s*$)"""
  """(?i)blocked="*(?:N\/A|None|({action}[^",]+))("|,|\s*$)"""
  """(?i)endpoint_machine="*(N\/A|({dest_host}[^",]+))("|,|\s*$)"""
  """(?i)endpoint_user_name="*\s*(N\/A|(({domain}[^\\]+)\\+)?({user}[^\s",]+))("|,|\s*$)"""
  """(?i)endpoint_user_name="*\s*(N\/A|({user}[^\s",@]+)@({domain}[^\s",@]+))"""
  """(?i)incident_snapshot=[^,]*?({alert_id}\d+),"""
  """(?i)machineIP="*(N\/A|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""
]
DupFields = [
  "alert_name->alert_type"
  "external_address->dest_email_address"
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
    "dest_host->dlpDeviceName"
    "action->dlpActionTaken"
  ]
  NameTemplate = "Vontu DLP Alert ${alert_name} found"
  ProjectName = "SOC"
  EntityFields = [
    {
      EntityType = "device"
      Name = "dest_address"
      Fields = [
        "dest_ip->ip_address"
        "dest_host->host_name"
      ]
    

}
```