#### Parser Content
```Java
{
Name = mcafee-ep-kv-email-send-fail-emailstatus
    Vendor = McAfee
    Product = McAfee Email Protection
    TimeFormat = "MM dd yyyy HH:mm:ss"
    Conditions = [ """Event='Email Status""" ]
    Fields = [
      """({time}\d\d \d\d \d\d\d\d \d\d:\d\d:\d\d)\s({host}\S+)\s(?i)<mail:info>""",
      """\sFrom=<({email_address}[^>,;]+)""",
      """\ssize=({bytes}\d+)""",
      """\ssource=({src_host}[^(,]+?)?\(({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """\snrcpts=({num_recipients}\d+)""",
      """\sto=<({dest_email_address}[^>,;]+)""",
      """\sto=<({email_recipients}[^>]+?)>""",
      """\sstatus='({result}[^']+?)'""",
      """\ssubject='({email_subject}[^']+?)'""",
      """\sattachment\(s\)='({email_attachments}[^']+?)'""",
      """\snumber-attachment\(s\)='({num_attachments}\d+)"""
    ]
	ParserVersion = "v1.0.0"
  

}
```