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
  """Sender:\s+({user}[^@]+)"""
  """Sender:\s+({src_email_address}[^,]+)"""
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