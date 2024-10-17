#### Parser Content
```Java
{
Name = "unix-unix-cef-email-send-receive-sendmail"
ParserVersion = "v1.0.0"
Vendor = "Unix"
Product = "Unix"
TimeFormat = "epoch"
Conditions = [
"""|Unix|Sendmail|"""
"""|Email """
""" Message|"""
]
Fields = [
"""\Wrt=({time}\d{13})"""
"""\Wdvc=({host}[^\s]+)"""
"""\Wdvchost=({host}[^\s]+)"""
"""CEF:([^\|]*\|){4}({alert_name}[^\|]+)"""
"""CEF:([^\|]*\|){6}({alert_severity}[^\|]+)"""
"""\WeventId=({alert_id}\d+)"""
"""\Wdsn\\=({result}[^\s,]+)"""
"""\Wsuser=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
"""\Wduser=\s*({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
"""\Wduser=\s*({email_recipients}[^\s]+)"""
"""\Wcn3=({num_recipients}\d+)"""
"""\Wsize\\=({bytes}\d+)"""
"""\Wproto=({protocol}[^\s,]+)"""
]
DupFields = [
"alert_name->alert_type"
]


}
```