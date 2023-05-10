#### Parser Content
```Java
{
Name = zeek-z-str-email-receive-success-brosmtp
  ParserVersion = v1.0.0
  Vendor = Zeek
  Product = Zeek
  TimeFormat = "epoch_sec"
  Conditions = [ """bro_smtp""" ]
  Fields = [
    """.*?({time}\d{10})\.\d{6}""",
    """(?:[^\t]+\t){11}.*?<({sender}[^\t>]+)""",
    """(?:[^\t]+\t){12}.*?<({user}[^>\t"]+)""",
    """(?:[^\t]+\t){12}({email_recipients}[^\t]+)""",
    """(?:[^\t]+\t){16}({email_subject}[^\t]+)""",
    """\tfrom .*?\(.*?(\[)?({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(\])?\)""",
    """(?=\tfrom.+?\tfrom)\tfrom.+?\tfrom .*?\(.*?(\[)?({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(\])?\)"""
    """({alert_name}bro_smtp)""",
  ]
  DupFields = [ "alert_name->alert_type", "user->orig_user", "sender->external_address" ]


}
```