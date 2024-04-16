#### Parser Content
```Java
{
Name = rsa-dlp-kv-email-send-success-smtp
Vendor = "RSA"
Product = "RSA DLP"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """DLP_EM:"""
  """protocol=smtp"""
  """RiskFactor="""
  """dlp_event_link"""
]
Fields = [
  """DLP_EM:\s*({host}[^\s]+)"""
  """Incident\s*:*\s*"({alert_name}[^"]+)"""
  """Severity=({alert_severity}[^\s]+)"""
  """User=(({domain}[^\\]+)\\)?({user}[\w\.\-]{1,40}\$?)\s+\w+="""
  """Policy=({alert_type}.+?)\s+\w+="""
  """userEmail=({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """sessionEmailMailto=({email_recipients}.+?)\s+\w+="""
  """sessionEmailMailto=({external_address}[^\s\^]+)"""
  """sessionEmailSubject=({email_subject}.+?)\s+\w+="""
]
ParserVersion = "v1.0.0"


}
```