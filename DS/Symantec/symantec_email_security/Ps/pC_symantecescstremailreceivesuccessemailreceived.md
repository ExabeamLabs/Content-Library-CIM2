#### Parser Content
```Java
{
Name = "symantec-esc-str-email-receive-success-emailreceived"
Vendor = "Symantec"
Product = "Symantec Email Security"
TimeFormat = "epoch_sec"
Conditions = [
  """|VERDICT|"""
  """|ORCPTS|"""
  """|ACCEPT|"""
  """|SENDER|"""
  """|RECEIVED"""
]
Fields = [
  """\s({host}[\w\.-]+)\s+\S+\[\d+\]:"""
  """\s*({time}\d{10})\|(|({alert_id}[^\|]+))\|VERDICT\|"""
  """\|ORCPTS\|({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)).*?)\|ACCEPT\|"""
  """\|ACCEPT\|({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}):({src_port}\d+)"""
  """\|SENDER\|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\|"""
]
ParserVersion = "v1.0.0"


}
```