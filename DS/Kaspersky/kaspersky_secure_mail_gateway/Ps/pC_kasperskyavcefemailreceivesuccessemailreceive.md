#### Parser Content
```Java
{
Name = "kaspersky-av-cef-email-receive-success-emailreceive"
Vendor = "Kaspersky"
Product = "Kaspersky Secure Mail Gateway"
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """Kaspersky|KSMG"""
  """destinationDnsDomain="""
]
Fields = [
  """shost=({dest_host}[^\s]+)"""
  """\srt=({time}\d{13})"""
  """\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\sdvchost=({host}[^\s]+)"""
  """\ssuser=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\s+(\w+=|$)"""
  """\sduser=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\s+(\w+=|$)"""
  """fsize=({bytes}\d+)"""
  """src=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """msg=\w+\s+"+({email_attachment}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```