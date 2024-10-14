#### Parser Content
```Java
{
Name = vectra-cs-kv-email-send-success-metadatasmtp
  TimeFormat = "epoch"
  Conditions = [ """COGNITO_STREAM""", """vectra_metadata_smtp""", """METADATA_SMTP""" ]
  Fields = ${VectraParserTemplates.vectra-meta-data.Fields} [
    """subject="({email_subject}[^"]+)"""",
    """mail_from="({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
    """rcpt_to="({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
    """msgid="<({message_id}[^"]+)>""""
  ]
  ParserVersion = "v1.0.0"

vectra-meta-data = {
  Vendor = Vectra
  Product = Vectra Cognito Stream
  TimeFormat = "epoch"
  Fields = [
    """\sts="+({time}\d{13})""",
    """id.orig_h="+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"+"""
    """id.orig_p="+({src_port}\d+)"+""",
    """id.resp_h="+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"+""",
    """id.resp_p="+({dest_port}\d+)"+""",
    """orig_hostname="+(null|((IP-)*((\d+\.){3}\d+|([A-Fa-f0-9]+:[A-Fa-f0-9:]+)|({src_host}[^"]+))))""""
    """resp_hostname="+(null|((IP-)*((\d+\.){3}\d+|([A-Fa-f0-9]+:[A-Fa-f0-9:]+)|({dest_host}[^"]+))))""""
  ]
 
}
```