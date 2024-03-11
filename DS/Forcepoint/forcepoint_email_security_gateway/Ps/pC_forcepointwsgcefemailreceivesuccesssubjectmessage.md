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
  """suser=({src_email_address}\S+)"""
  """suser=({external_address}\S+)"""
  """duser=({email_recipients}\S+)"""
  """msg=({email_subject}.+?)\s*(\w+=|$)"""
  """in=({bytes}\d+)"""
]
DupFields = [
  "src_email_address->user"
  "email_recipients->dest_email_address"
]
ParserVersion = "v1.0.0"


}
```