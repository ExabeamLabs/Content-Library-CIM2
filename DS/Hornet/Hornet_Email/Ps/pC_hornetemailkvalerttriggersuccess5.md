#### Parser Content
```Java
{
Name = hornet-email-kv-alert-trigger-success-5
  ParserVersion = v1.0.0
  Vendor = Hornet
  Product = Hornet Email
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """main_domain=""", """owner=""", """smtp_code=""", """crypt_type=""", """from_hdr=""", """update_nr=""", """type=5""" ]
  Fields = [
    """date=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
    """reason="({alert_name}[^"]+)""",
    """type=({alert_type}5)""",
    """msgid="({alert_id}[^"]+)""",
    """dir=({direction}1|2)""",
    """main_domain=({domain}[^=]+?)\s*(\w+=|$)""",
    """from=({email_address}[^@\s]+?@[^\s]+)""",
    """to=({dest_email_address}[^@\s]+?@[^\s]+)""",
    """src_host=((?i)unknown|({src_host}[^\s]+))""",
    """src_ip=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """dst_ip=(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[^\s]+))""",
    """attachments="[^0"]#({email_attachments}[^"]+)""",
    """subject="[ \s]*({email_subject}[^"]+?)[ \s]*"""",
  ]
  DupFields = [ "alert_type->alert_severity" ]


}
```