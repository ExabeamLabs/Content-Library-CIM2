#### Parser Content
```Java
{
Name = microsoft-exchange-kv-email-receive-incoming
Vendor = Microsoft
Product = Microsoft Exchange
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """message-subject="""
  """TOTAL-HUB="""
  """directionality=Incoming"""
]
Fields = [
  """client-ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """SourceIp=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """server-ip=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """server-hostname=({dest_host}[\w.\-]+)"""
  """date-time=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """client-hostname=({src_host}[\w.\-]+)"""
  """\tsource=(?:|({alert_name}.+?))\t[\w\-]+="""
  """event-id=({result}\w+)"""
  """\tinternal-message-id=(?:|({alert_id}.+?))\t[\w\-]+="""
  """recipient-address=({email_recipients}\S+)"""
  """recipient-address=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)|({dest_user_full_name}\w+(\s+\w+)+))"""
  """total-bytes=({bytes}\d+)"""
  """recipient-count=({num_recipients}\d+)"""
  """message-subject="*({email_subject}.+?)"*\s+((\w+-)*\w+=|$)"""
  """sender-address=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """directionality=({direction}\w+)"""
]
DupFields = [
  "alert_name->alert_type"
  "dest_email_address->orig_user"
]
ParserVersion = "v1.0.0"


}
```