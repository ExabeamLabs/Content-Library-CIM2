#### Parser Content
```Java
{
Name = hornet-email-kv-alert-trigger-success-5
  ParserVersion = v1.0.0
  Vendor = Hornet
  Product = Hornetsecurity Cloud Email Security Services
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """main_domain=""", """owner=""", """smtp_code=""", """crypt_type=""", """from_hdr=""", """update_nr=""", """type=5""" ]
  Fields = [
    """date=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
    """reason="({alert_name}[^"]+)""",
    """type=({alert_type}5)""",
    """msgid="({alert_id}[^"]+)""",
    """dir=({direction}1|2)""",
    """main_domain=({domain}[^=]+?)\s*(\w+=|$)""",
    """from=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """to=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """src_host=((?i)unknown|({src_host}[^\s]+))""",
    """src_ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """dst_ip=(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[^\s]+))""",
    """attachments="[^0"]#({email_attachments}[^"]+)""",
    """subject="[ \s]*({email_subject}[^"]+?)[ \s]*"""",
  ]
  DupFields = [ "alert_type->alert_severity" ]


}
```