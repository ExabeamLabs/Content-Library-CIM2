#### Parser Content
```Java
{
Name = microsoft-o365-kv-email-quarantined
Vendor = Microsoft
Product = Microsoft 365
TimeFormat = "MM/dd/yyyy HH:mm:ss"
Conditions = [
  """@{Status="""
  """; SenderAddress="""
]
Fields = [
  """({host}[\w.\-]+)\s+(\S+\s+){4}@\{Status="""
  """Status=({result}[^;]+)"""
  """Received=({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d)"""
  """SenderAddress=({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """RecipientAddress=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """RecipientAddress=({email_recipients}[^;]+)"""
  """Size=({bytes}\d+)"""
  """Subject=({email_subject}.+?)\s*\}"""
]
ParserVersion = "v1.0.0"


}
```