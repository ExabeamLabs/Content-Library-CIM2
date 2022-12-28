#### Parser Content
```Java
{
Name = microsoft-o365-kv-email-delivered
Vendor = Microsoft
Product = Microsoft 365
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
  """SIP=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """DIP=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """SUBJECT=(|({email_subject}.+?))\s+\w+="""
  """STATUS=({result}[^\s]+)"""
  """SIZE=({bytes}\d+)"""
  """SESSID=({message_id}[^\s]+)"""
]
ParserVersion = "v1.0.0"


}
```