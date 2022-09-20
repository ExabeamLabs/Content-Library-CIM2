#### Parser Content
```Java
{
Name = microsoft-o365-kv-email-delivered
Vendor = Microsoft
Product = Office 365
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """O365 Messages logrhythm:"""
  """TS="""
  """SESSID="""
]
Fields = [
  """TS=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """RECIPIENT=({dest_email_address}[^\s]+)"""
  """SENDER=({email_address}[^\s]+)"""
  """SIP=({src_ip}[a-fA-F\d.:]+)"""
  """DIP=({dest_ip}[a-fA-F\d.:]+)"""
  """SUBJECT=(|({email_subject}.+?))\s+\w+="""
  """STATUS=({result}[^\s]+)"""
  """SIZE=({bytes}\d+)"""
  """SESSID=({message_id}[^\s]+)"""
]
ParserVersion = "v1.0.0"


}
```