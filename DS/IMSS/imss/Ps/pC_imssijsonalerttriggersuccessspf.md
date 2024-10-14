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
"""({time}\d{4}\/\d\d\/\d\d \d+:\d+:\d+ \w+(\+|\-)\d+:\d+)\s\S+\s(|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))\s(|"?({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^\s]*?)"?)\s(|"?({email_subject}.+?)"?)\s\d\s(|({alert_name}[^\s]+))\s\d+\s[^\s]*?\s({bytes}\d+\.?\d*)\s([^\s]*?\s){19}(|({email_attachments}[^\s]+))""",

}
```