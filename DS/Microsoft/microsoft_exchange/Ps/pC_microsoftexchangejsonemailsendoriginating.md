#### Parser Content
```Java
{
Name = microsoft-exchange-json-email-send-originating
Vendor = Microsoft
Product = Microsoft Exchange
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
Conditions = [
  """event_id":"""
  """directionality":"Originating""""
]
Fields = [
  """date_time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\d)Z"""
  """client_ip":"(?:|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)","""
  """client_hostname":"(?:|({src_host}[^"]+))","""
  """server_ip":"(?:|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)","""
  """server_hostname":"(?:|({dest_host}[^"]+))","""
  """exchange_source":"(?:|({alert_name}[^"]+))","""
  """event_id":"(?:|({action}[^"]+))","""
  """internal_message_id":"*(?:|({alert_id}[^",]+))"*,"""
  """recipient_address":"(?:|({email_recipients}[^"]+))","""
  """total_bytes":"*(?:|({bytes}\d+))"*,"""
  """recipient_count":"*(?:|({num_recipients}\d+))"*,"""
  """message_subject":"(?:|({email_subject}[^"]+))","""
  """sender_address":"(?:|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))","""
  """return_path":"(?:|<>|({return_path}[^"]+))","""
]
DupFields = [
  "alert_name->alert_type"
]
ParserVersion = "v1.0.0"


}
```