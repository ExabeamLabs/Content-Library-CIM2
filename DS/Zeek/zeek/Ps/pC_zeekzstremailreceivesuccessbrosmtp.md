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
    """(?:[^\t]+\t){11}.*?<({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """(?:[^\t]+\t){12}.*?<({orig_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """(?:[^\t]+\t){12}({email_recipients}[^\t]+)""",
    """(?:[^\t]+\t){16}({email_subject}[^\t]+)""",
    """\tfrom .*?\(.*?(\[)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?(\])?\)""",
    """(?=\tfrom.+?\tfrom)\tfrom.+?\tfrom .*?\(.*?(\[)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?(\])?\)"""
    """({alert_type}({alert_name}bro_smtp))""",
  ]


}
```