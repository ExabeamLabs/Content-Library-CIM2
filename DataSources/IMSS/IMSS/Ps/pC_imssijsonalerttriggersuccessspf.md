#### Parser Content
```Java
{
Name = imss-i-json-alert-trigger-success-spf
  Product = IMSS
  ParserVersion = "v1.0.0"
  Conditions = [ """SPFレコードチェック""" ]

imss-email-alert = {
Vendor = IMSS
TimeFormat = "yyyy/MM/dd HH:mm:ss zZ"
Fields = [
"""({time}\d{4}\/\d\d\/\d\d \d+:\d+:\d+ \w+(\+|\-)\d+:\d+)\s\S+\s(|({sender}[^\s]+))\s(|"?({recipients}({dest_email_address}[^;\s@]+@[^;\s"]+)[^\s]*?)"?)\s(|"?({email_subject}.+?)"?)\s\d\s(|({alert_name}[^\s]+))\s\d+\s[^\s]*?\s({bytes}\d+\.?\d*)\s([^\s]*?\s){19}(|({email_attachments}[^\s]+))""",
]
DupFields = [ "sender->email_address", "dest_email_address->external_address" 
}
```