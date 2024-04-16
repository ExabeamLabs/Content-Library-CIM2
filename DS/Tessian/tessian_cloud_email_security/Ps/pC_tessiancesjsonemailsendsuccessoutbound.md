#### Parser Content
```Java
{
Name = tessian-ces-json-email-send-success-outbound
  Conditions = [ """.tessian-platform.""", """"recipients":{""", """"transmitter":"""", """"from":"""", """"to":[""", """::outbound-""" ]
  Fields = ${TessianParserTemplates.tessian-dlp-email-alert.Fields} [
    """::({direction}outbound)\-"""
  ]
  ParserVersion = v1.0.0

tessian-dlp-email-alert = {
    Vendor = Tessian
    Product = Tessian Cloud Email Security
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
    Fields = [
      """"created_at":"({time}\d{4}-\d{1,2}-\d{1,2}T\d\d:\d\d:\d\d\.\d{1,6}Z)"""",	
      """"tessian_action":"({alert_name}[^"]+)"""",
      """"threat_types":\["({alert_name}[^"]+)"\]""",
      """"tessian_id":"({alert_id}[^"]+)"""",
      """"confidence":"({alert_severity}[^"]+)"""",
      """"message_id":"({message_id}[^"]+)"""",
      """"transmitter":"({src_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""",
      """"from":"({src_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""",
      """"recipients":\{"all":\[({email_recipients}"'?({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)'?[^\]]+)""",
      """"to":\["({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""",
      """"subject":"\s*({email_subject}[^"]+?)\s*"""",
      """"final_outcome":"({result}[^"]+)"""",
      """"attachments":\{"names":\[({email_attachments}"({email_attachment}[^"]+)[^\]\}]+)""",
      """"cc":\[({cc}[^\]]+)\]""",
      """"bcc":\[({bcc}[^\]]+)\]""",
      """"bytes":({bytes}\d+),"""
    ]
    DupFields = ["alert_name->alert_type"
}
```