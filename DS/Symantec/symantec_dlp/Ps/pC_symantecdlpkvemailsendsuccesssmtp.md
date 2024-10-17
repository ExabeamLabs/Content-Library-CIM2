#### Parser Content
```Java
{
Name = "symantec-dlp-kv-email-send-success-smtp"
Vendor = "Symantec"
Product = "Symantec DLP"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """protocol=SMTP"""
  """incident_id="""
  """sender="""
  """recipient="""
]
Fields = [
  """({host}[\w.\-]+)\s+incident_id="""
  """recipient=({email_recipients}[^,@]+@[^,]+),"""
  """sender=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)),"""
  """Subject=({email_subject}.+?)\s*,(\s+\w+=|\s*$)"""
  """blocked=({action}\w+)"""
  """Attachment_Filename=({email_attachments}.+?)\s*,(\s+\w+=|\s*$)"""
  """incident_id=({alert_id}\d+)"""
  """protocol=({protocol}.*?)\s+\w+="""
]
DupFields = [
  "email_recipients->dest_email_address"
]
ParserVersion = "v1.0.0"


}
```