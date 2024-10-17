#### Parser Content
```Java
{
Name = "unix-sm-kv-email-receive-success-sentemail"
Vendor = "Unix"
Product = "Unix Sendmail"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """[Web] Sent e-mail"""
]
Fields = [
  """\]:\s*\(({src_ip}[a-fA-F:\d.]+).*?\[Web\] Sent e-mail"""
  """User:\s*({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|\)]+))"""
  """\]:\s*\(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?.*?\[Web\] Sent e-mail"""
  """Subject:\s*({email_subject}.+?);\s*To:"""
  """To:\s*({email_recipients}.+?)\s+with files:"""
  """To:\s*({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """files:\s*.*?[\\\/]*({file_name}[^\\\/]+?)\s*\("""
  """files:\s*({email_attachments}.+?)\s*$"""
  """files:\s*.*?[\\\/]*({email_attachment}.+?)\s*\(({bytes}[\d.]+)\s*({bytes_unit}[^\s\)]+)"""
]
ParserVersion = "v1.0.0"


}
```