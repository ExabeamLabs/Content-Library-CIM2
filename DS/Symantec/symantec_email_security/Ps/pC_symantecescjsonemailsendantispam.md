#### Parser Content
```Java
{
Name = symantec-esc-json-email-send-antispam
Vendor = "Symantec"
Product = "Symantec Email Security"
TimeFormat = "epoch"
Conditions = [
  """CEF"""
  """|Symantec|Symantec Email Security.cloud|"""
]
Fields = [
  """"logging_device_ip ":"({host}[^"]+)""""
  """\Wrt=({time}\d{13})"""
  """"sender_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """"header_subject":"({email_subject}[^"]+)"""
  """"smtp_to":\[({email_recipients}"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)).*?)\]"""
  """\Wsuser=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """"size":"?({bytes}\d+)"""
  """\Wsuser=({email_address}\S+)"""
  """"dkim":"({action}[^"]+)"""
  """"event_id":({alert_id}\d+)"""
  """"severity_id":({alert_severity}\d+)"""
  """"feature_name":"({alert_type}[^"]+)""""
  """"threat":\{"name":"({alert_name}[^"]+)"""
  """"product_name":"({product_name}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```