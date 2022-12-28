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
  """SenderAddress=({email_address}[^;@]+@[^;]+)"""
  """RecipientAddress=({dest_email_address}[^;@]+@[^;]+)"""
  """RecipientAddress=({email_recipients}[^;]+)"""
  """Size=({bytes}\d+)"""
  """Subject=({email_subject}.+?)\s*\}"""
]
ParserVersion = "v1.0.0"


}
```