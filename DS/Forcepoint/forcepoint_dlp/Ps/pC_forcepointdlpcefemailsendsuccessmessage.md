#### Parser Content
```Java
{
Name = "forcepoint-dlp-cef-email-send-success-message"
Vendor = "Forcepoint"
Product = "Forcepoint DLP"
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """|Forcepoint|AP-EMAIL|"""
  """|Message|Message|"""
  """ cs6="""
]
Fields = [
  """\Wrt=({time}\d{13})"""
  """\Wdvc=({host}[\d.]+)"""
  """\Wdvchost=({host}[\w\-.]+)"""
  """\WeventId=({alert_id}\d+)"""
  """\Wmsg=\s*({email_subject}.+?)\s+(\w+=|$)"""
  """\Wout=({bytes}\d+)"""
  """\Wsuser=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """\Wduser=({email_recipients}.+?)\s+(\w+=|$)"""
  """\Wduser=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """\Wfname=({email_attachments}.*?)\s+(\w+=|$)"""
  """\Wcs6=({direction}.+?)\s+(\w+=|$)"""
  """CEF:([^\|]*\|){6}({alert_severity}[^\|]+)"""
]
ParserVersion = "v1.0.0"


}
```