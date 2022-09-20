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
  """client_ip":"(?:|({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))","""
  """client_hostname":"(?:|({src_host}[^"]+))","""
  """server_ip":"(?:|({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))","""
  """server_hostname":"(?:|({dest_host}[^"]+))","""
  """exchange_source":"(?:|({alert_name}[^"]+))","""
  """event_id":"(?:|({action}[^"]+))","""
  """internal_message_id":"*(?:|({alert_id}[^",]+))"*,"""
  """recipient_address":"(?:|({email_recipients}[^"]+))","""
  """recipient_address":"(?:|({external_address}[^,;@]+@[^;,"']+))","""
  """total_bytes":"*(?:|({bytes}\d+))"*,"""
  """recipient_count":"*(?:|({num_recipients}\d+))"*,"""
  """message_subject":"(?:|({email_subject}[^"]+))","""
  """sender_address":"(?:|({email_address}[^"]+))","""
  """return_path":"(?:|<>|({return_path}[^"]+))","""
]
DupFields = [
  "alert_name->alert_type"
]
ParserVersion = "v1.0.0"


}
```