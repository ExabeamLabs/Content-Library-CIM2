#### Parser Content
```Java
{
Name = symantec-dlp-str-email-send-protectmanager
Vendor = "Symantec"
Product = "Symantec DLP"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """/ProtectManager/IncidentDetail.do"""
  """^^"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
  """({host}[\w.\-]+)\s+({alert_name}[^\s\^]+)\^\^({alert_id}\d+)\^\^({additional_info}[^\^]+)\^\^[^\^]*\^\^({email_recipients}({dest_email_address}[^\^,]+)[^\^]*)\^\^({src_email_address}[^\^]+)\^\^({alert_severity}[^\^]+)\^\^({email_subject}[^\^]+)\^\^(N/A|({object}[^\^]+))\^\^([^\^]*\^\^){9}({protocol}[^\^]+?)\s*(\^|$)"""
  """\d\d:\d\d:\d\d\s+({host}[\w.\-]+)\s+({action}[^\^]+?)\^\^"""
  """\d\d:\d\d:\d\d\s+[\w.\-]+\s+[^\^]*?\^\^({alert_id}[^\^]+)"""
  """\d\d:\d\d:\d\d\s+[\w.\-]+\s+([^\^]*?\^\^){2}({url}(\w+:\/+)?({web_domain}[^\\\/]+)[^\^]+)"""
  """\d\d:\d\d:\d\d\s+({host}[\w.\-]+)\s+([^\^]*?\^\^){4}({email_recipients}({dest_email_address}[^\^,]+)[^\^]*)"""
  """\d\d:\d\d:\d\d\s+[\w.\-]+\s+([^\^]*?\^\^){5}({src_email_address}[^\^]+)"""
  """\d\d:\d\d:\d\d\s+[\w.\-]+\s+([^\^]*?\^\^){6}({alert_severity}[^\^]+)"""
  """\d\d:\d\d:\d\d\s+[\w.\-]+\s+([^\^]*?\^\^){7}({email_subject}[^\^]+)"""
  """\d\d:\d\d:\d\d\s+[\w.\-]+\s+([^\^]*?\^\^){13}({alert_name}[^\^]+)"""
  """\d\d:\d\d:\d\d\s+[\w.\-]+\s+([^\^]*?\^\^){14}({alert_type}[^\^]+)"""
  """\d\d:\d\d:\d\d\s+[\w.\-]+\s+([^\^]*?\^\^){18}({protocol}[^\^]+?)\s*(\^|$)"""
  """\^\^\?{3}\s*({action}\S+)"""
]
DupFields = [
  "src_email_address->original_user"
]
SOAR {
  IncidentType = "dlp"
  DupFields = [
    "time->startedDate"
    "vendor->source"
    "rawLog->sourceInfo"
    "email_address->dlpUser"
    "alert_name->dlpPolicy"
    "alert_severity->sourceSeverity"
    "action->dlpActionTaken"
  ]
  NameTemplate = "Vontu DLP Alert ${alert_name} found"
  ProjectName = "SOC"
  EntityFields = [
    {
      EntityType = "user"
      Name = "windows_id"
      Fields = [
        """email_address->windows_id"""
      ]
    

}
```