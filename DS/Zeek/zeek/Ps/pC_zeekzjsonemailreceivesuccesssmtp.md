#### Parser Content
```Java
{
Name = "zeek-z-json-email-receive-success-smtp"
Vendor = "Zeek"
Product = "Zeek"
TimeFormat = "epoch"
Conditions = [
  """bro_smtp"""
  """"id.orig_h"""
  """"id.resp_h"""
]
Fields = [
  """"to\\"+:\[\\"+({email_address}[^"\\]+)"""
  """"id.orig_h\\"+:\\"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"id.resp_h\\"+:\\"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """"from\\"+:\\"+({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """"to\\"+:\[({email_recipients}\\"+({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^\]]+)\]"""
  """"subject\\"+:\\"+({email_subject}[^"\\]+)"""
  """"rawmsghostname":"({host}[^"]+)"""
  """"meta_ts"+:({time}\d{13})"""
]
DupFields = [
  "src_email_address->external_address"
]
ParserVersion = "v1.0.0"


}
```