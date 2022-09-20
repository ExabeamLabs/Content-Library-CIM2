#### Parser Content
```Java
{
Name = symantec-esc-json-email-send-antispam
Vendor = "Symantec"
Product = "Symantec Email Security.cloud"
TimeFormat = "epoch"
Conditions = [
  """CEF"""
  """|Symantec|Symantec Email Security.cloud|"""
]
Fields = [
  """"logging_device_ip ":"({host}[^"]+)""""
  """\Wrt=({time}\d+)"""
  """"sender_ip":"({src_ip}[^"]+)""""
  """"header_subject":"({email_subject}[^"]+)"""
  """"smtp_to":\[({email_recipients}"({dest_email_address}[^"@]+@[^"@]+).*?)\]"""
  """\Wsuser=({email_address}[^=@]+@[^\s]+)"""
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