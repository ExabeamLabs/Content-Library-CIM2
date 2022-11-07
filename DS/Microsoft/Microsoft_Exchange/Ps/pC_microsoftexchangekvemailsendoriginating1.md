#### Parser Content
```Java
{
Name = microsoft-exchange-kv-email-send-originating-1
Vendor = Microsoft
Product = Microsoft Exchange
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """message-subject="""
  """TOTAL-HUB="""
  """directionality=Originating"""
]
Fields = [
  """client-ip=({src_ip}[a-fA-F\d.:]+)"""
  """SourceIp=({src_ip}[a-fA-F\d.:]+)"""
  """server-ip=({dest_ip}[a-fA-F\d.:]+)"""
  """server-hostname=({dest_host}[\w.\-]+)"""
  """date-time=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """client-hostname=({src_host}[\w.\-]+)"""
  """\tsource=(?:|({alert_name}.+?))\t[\w\-]+="""
  """event-id=({action}\w+)"""
  """\tinternal-message-id=(?:|({alert_id}.+?))\t[\w\-]+="""
  """recipient-address=({email_recipients}\S+)"""
  """recipient-address=({dest_email_address}[^\s;@]+@[^@\s;]+)"""
  """total-bytes=({bytes}\d+)"""
  """recipient-count=({num_recipients}\d+)"""
  """message-subject="*({email_subject}.+?)"*\s+((\w+-)*\w+=|$)"""
  """sender-address=({email_address}\S+)"""
  """directionality=({direction}\w+)"""
]
DupFields = [
  "alert_name->alert_type"
  "dest_email_address->external_address"
  "email_address->user"
  "email_address->orig_user"
]
ParserVersion = "v1.0.0"


}
```