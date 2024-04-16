#### Parser Content
```Java
{
Name = "symantec-dlp-kv-email-send-success-emailsend-3"
Vendor = "Symantec"
Product = "Symantec DLP"
TimeFormat = "MMM dd, yyyy HH:mm:ss a"
Conditions = [
  """Incident_Snapshot: """
  """Endpoint_Machine: """
  """Incident_ID: """
  """Policy: """
]
Fields = [
  """({host}[^\s]+)\s*Incident_Snapshot:"""
  """Occurred:\s*({time}\w+ \d+, \d\d\d\d \d+:\d+:\d+ (?i)(am|pm))"""
  """Machine_IP:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """Severity:\s*({alert_severity}[^,]+)"""
  """Incident_ID:\s*({alert_id}\d+)"""
  """Status:\s*(N\/A|({result}[^,]+))"""
  """Endpoint_Username:\s*(N\/A|(({domain}[^\\,]+)\\+)?({user}[\w\.\-]{1,40}\$?))"""
  """Endpoint_Machine:\s*(N\/A|({dest_host}[^,]+))"""
  """Protocol:\s*(N\/A|({protocol}[^,]+))"""
  """Recipients:\s*(N\/A|Unknown|({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^:]*),[^:]+Subject:)"""
  """Subject:\s*(N\/A|({email_subject}[^,]+?))\s*,"""
  """Sender:\s*(N\/A|({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))),[^:]+Recipients:"""
  """Policy:\s*({alert_name}[^,]+)"""
  """File_Full_Path:\s*(N\/A|(|({file_path}({file_dir}[^"]*?[\\\/]*)(|({file_name}[^\\\/"]*?(\.({file_ext}[^\\\/\.\s"]*))?)))))"*\s*$"""
  """(?i)Incident_Snapshot:\s*({url}[^,]*)"""
  """(?i)recipients:\s*[^@]+@({external_domain}[^,"@]+)("|,|\s*$)"""
]
DupFields = [
  "dest_email_address->external_address"
  "email_recipients->target"
]
ParserVersion = "v1.0.0"


}
```