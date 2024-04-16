#### Parser Content
```Java
{
Name = symantec-dlp-kv-email-send-confidentialdata
Vendor = "Symantec"
Product = "Symantec DLP"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """Policy Violated: """
  """Protocol: SMTP,"""
  """Subject: """
  """Blocked: """
]
Fields = [
  """\s({host}[^.\s]+)(\.\w+)*\s*(Message =)? ID:\s({alert_id}\d+)"""
  """Sender:\s+({user}[\w\.\-]{1,40}\$?)"""
  """Sender:\s+({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """Subject:\s+({email_subject}.+?),\s+Target:"""
  """Recipient:\s+({email_recipients}.+?),\s+Sender:"""
  """Severity:\s+({alert_severity}.+?),\s+Subject:"""
  """Policy Violated:\s+({alert_name}.+?),\s+Count:"""
  """Protocol:\s+(({alert_type}[^,]+))"""
  """Protocol:\s+(({protocol}[^,]+))"""
  """({direction}o)"""
  """\sBlocked:\s+({action}[^\s,]+)"""
  """Recipient:\s*({email_recipients}[^",;]+@[^",;]+[^"]*),\s+Sender:"""
]
ParserVersion = "v1.0.0"


}
```