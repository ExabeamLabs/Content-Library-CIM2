#### Parser Content
```Java
{
Name = "forcepoint-dlp-cef-email-receive-success-policyclean"
Vendor = "Forcepoint"
Product = "Forcepoint DLP"
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """|Forcepoint|AP-EMAIL|"""
  """|Policy|Clean|"""
]
Fields = [
  """CEF:([^\|]*\|){6}({alert_severity}[^\|]+)"""
  """\Wrt=({time}\d{13})"""
  """\Wdvc=({host}[\d.]+)"""
  """\Wdvchost=({host}[\w\-.]+)"""
  """\Win=({bytes}\d+)"""
  """\Wduser=({dest_email_address}[^\s=,;]+)"""
  """\WdeviceDirection=(|({direction}.+?))\s+(\w+=|$)"""
  """\WhybridSpamScore=({spam_score}[\+\-]\d+)"""
  """\Wact=({action}\d+)"""
  """\WmessageId=({alert_id}\d+)"""
]
ParserVersion = "v1.0.0"


}
```