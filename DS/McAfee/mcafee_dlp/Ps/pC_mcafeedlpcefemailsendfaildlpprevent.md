#### Parser Content
```Java
{
Name = mcafee-dlp-cef-email-send-fail-dlpprevent
    Vendor = McAfee
    Product = McAfee DLP
    TimeFormat = "epoch"
    Conditions = [ """CEF:""", """|McAfee|DLP Prevent|"""]
    Fields = [
      """\w{3} \d{1,2} \d{1,2}:\d{1,2}:\d{1,2}\s*({host}[\w\-\.]+)\s*""",
      """(\s|\|)rt=({time}\d{13})""",
      """CEF:([^|]+?\|){5}({alert_type}[^|]+)""",
      """CEF:([^|]+?\|){6}({alert_severity}[^|]+)""",
      """(\s|\|)app=({protocol}.+?)\s+\w+=""",
      """(\s|\|)msg=(\s+|(({alert_name}.+?)\s*))(\w+=|$)""",
      """(\s|\|)src=({src_ip}(\d{1,3}\.){3}\d{1,3})""",
      """(\s|\|)shost=({src_host}[^\s]+)""",
      """(\s|\|)suser=<?({email_address}[^\s@<>]+?@[^\s@<>]+)"""
      """(\s|\|)duser=<?({dest_email_address}[^\s@<>]+?@[^\s@<>]+)"""
      """(\s|\|)duser=(\s+|(({email_recipients}.+?)\s*))(\w+=|$)""",
      """(\s|\|)fsize=({bytes}\d+)""",
      """\scs4=(\s+|(({email_attachments}.+?)\s*))(\w+=|$)""",
      """\scs6=(\s+|(({email_subject}.+?)\s*))(\w+=|$)""",
      """\scn3=({num_recipients}\d+)"""
      """(\s|\|)sMcAfeeDLPEmailSender=<?({email_address}[^\s@<>]+?@[^\s@<>]+)"""
      """(\s|\|)sMcAfeeDLPEmailRecipients=<?({dest_email_address}[^\s@<>]+?@[^\s@<>]+)"""
      """\sMcAfeeDLPEmailRecipients=(\s+|((email_recipients}.+?)\s*))(\w+=|$)"""
      """\sMcAfeeDLPHostDomainName =({domain}[\w\-\.]+?)\s*(\w+=|$)"""
      """\sMcAfeeDLPHostName =({host}[\w\-\.]+?)\s*(\w+=|$)"""
      """({additional_info}Unable to deliver message.)"""
    ]
    DupFields = [ "dest_email_address->external_address" ]
	ParserVersion = "v1.0.0"
  

}
```