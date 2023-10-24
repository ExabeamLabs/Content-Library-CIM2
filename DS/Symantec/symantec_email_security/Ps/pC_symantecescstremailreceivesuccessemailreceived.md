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
  """\|ORCPTS\|({email_recipients}({dest_email_address}[^\|]+).*?)\|ACCEPT\|"""
  """\|ACCEPT\|({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}):({src_port}\d+)"""
  """\|SENDER\|({src_email_address}[^@\|]+@[^@\|]+)\|"""
]
DupFields = [
  "src_email_address->external_address"
]
ParserVersion = "v1.0.0"


}
```