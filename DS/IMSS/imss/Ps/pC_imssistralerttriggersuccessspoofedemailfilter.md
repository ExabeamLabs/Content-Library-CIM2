#### Parser Content
```Java
{
Name = imss-i-str-alert-trigger-success-spoofedemailfilter
  ParserVersion = v1.0.0
  Vendor = IMSS
  Product = IMSS
  Conditions = [ """詐称メールフィルタ""" ]
  TimeFormat = "yyyy/MM/dd HH:mm:ss zZ"
  Fields = [
    """({time}\d{4}\/\d\d\/\d\d \d+:\d+:\d+ \w+(\+|\-)\d+:\d+)\s\S+\s(|({email_address}[^\s]+))\s(|"?({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^\s]*?)"?)\s(|"?({email_subject}.+?)"?)\s\d\s(|({alert_name}[^\s]+))\s\d+\s[^\s]*?\s({bytes}\d+\.?\d*)\s([^\s]*?\s){19}(|({email_attachments}[^\s]+))""",
  ]


}
```