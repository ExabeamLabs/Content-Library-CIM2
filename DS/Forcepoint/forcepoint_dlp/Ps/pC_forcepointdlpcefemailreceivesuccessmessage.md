#### Parser Content
```Java
{
Name = "forcepoint-dlp-cef-email-receive-success-message"
Vendor = "Forcepoint"
Product = "Forcepoint DLP"
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """|Forcepoint|AP-EMAIL|"""
  """|Message|Message|"""
]
Fields = [
  """CEF:([^\|]*\|){6}({alert_severity}[^\|]+)"""
  """\Wrt=({time}\d{13})"""
  """\Wdvc=({host}[\d.]+)"""
  """\Wdvchost=({host}[\w\-.]+)"""
  """\Wmsg=\s*({email_subject}.+?)\s+(\w+=|$)"""
  """\Win=({bytes}\d+)"""
  """\Wfname=(|({email_attachments}.*?))\s+(\w+=|$)"""
  """\Wfrom="*([^"@\s]+@[^"@\s]+|({full_name}[^"<@]+?))"*\s+<({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|\>]+))"""
  """\Wsuser=(|({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|\>]+)))"""
  """\WtrueSrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\WmessageId=({alert_id}\d+)"""
  """\Wcc=(|({cc}[^\s]+))"""
  """\Wurl="(|({url}[^"]+))""""
]
ParserVersion = "v1.0.0"


}
```