#### Parser Content
```Java
{
Name = vectra-cs-kv-email-send-success-metadatasmtp
  TimeFormat = "epoch_sec"
  Conditions = [ """COGNITO_STREAM""", """vectra_metadata_smtp""", """METADATA_SMTP""" ]
  Fields = ${VectraParserTemplates.vectra-meta-data.Fields} [
    """subject="({log_subject}[^"]+)"""",
    """mail_from="({email_address}[^"@]+@[^"]+)"""",
    """rcpt_to="({dest_email_address}[^"@]+@[^"]+)"""",
    """msgid="<({message_id}[^"]+)>""""
  ]
  ParserVersion = "v1.0.0"

vectra-meta-data = {
  Vendor = Vectra
  Product = Cognito Stream
  TimeFormat = "epoch"
  Fields = [
    """\sts="+({time}\d+)""",
    """id.orig_h="+({src_ip}\d+.\d+.\d+.\d+)"+"""
    """id.orig_p="+({src_port}\d+)"+""",
    """id.resp_h="+({dest_ip}\d+.\d+.\d+.\d+)"+""",
    """id.resp_p="+({dest_port}\d+)"+""",
    """orig_hostname="+(null|((IP-)*((\d+\.){3}\d+|([A-Fa-f0-9]+:[A-Fa-f0-9:]+)|({src_host}[^"]+))))""""
    """resp_hostname="+(null|((IP-)*((\d+\.){3}\d+|([A-Fa-f0-9]+:[A-Fa-f0-9:]+)|({dest_host}[^"]+))))""""
  ]
 
}
```