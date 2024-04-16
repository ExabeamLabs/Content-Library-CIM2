#### Parser Content
```Java
{
Name = "symantec-dlp-kv-email-send-success-emailsend"
Vendor = "Symantec"
Product = "Symantec DLP"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """,blocked=""""
  """,rules=""""
  """,subject=""""
  """incident_id=""""
  """,mtchcnt=""""
]
Fields = [
  """({host}[\w\-.]+)\s+incident_id="""
  """\Wincident_id="({alert_id}\d+)"""
  """\Wblocked="({action}[^",]+)"""
  """\Wpolicy="({alert_name}[^"]+)"""
  """\Wpolicy="[^"\-]+\-\s*({alert_type}[^"]+)"""
  """\Wpolicy="[^"\-]+\-\s*({protocol}[^"]+)"""
  """\Wrecipients="({email_recipients}[^"]+)"""
  """\Wrecipients="({external_address}[^,"]+)"""
  """\Wsender="({user}[\w\.\-]{1,40}\$?)"""
  """\Wsender="({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """\Wseverity="({alert_severity}[^"]+)"""
  """\Wsubject="({email_subject}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```