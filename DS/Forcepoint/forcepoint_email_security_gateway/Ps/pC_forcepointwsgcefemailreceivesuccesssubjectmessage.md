#### Parser Content
```Java
{
Name = forcepoint-wsg-cef-email-receive-success-subjectmessage
Vendor = "Forcepoint"
Product = "Forcepoint Email Security Gateway"
TimeFormat = "epoch"
Conditions = [
  """|Websense|ESG|"""
  """|Message|Message|"""
  """dvc="""
  """msg="""
]
Fields = [
  """({host}[\w\-.]+)\s+CEF:"""
  """dvc=({host}[a-fA-F:\d.]+)"""
  """dvchost=({host}[\w\-.]+)"""
  """rt=({time}\d{13})"""
  """suser=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """duser=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """msg=({email_subject}.+?)\s*(\w+=|$)"""
  """in=({bytes_in}\d+)"""
]
DupFields = [
  "dest_email_address->email_recipients"
]
ParserVersion = "v1.0.0"


}
```