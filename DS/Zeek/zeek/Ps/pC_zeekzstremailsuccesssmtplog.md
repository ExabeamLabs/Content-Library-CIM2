#### Parser Content
```Java
{
Name = zeek-z-str-email-success-smtplog
  ParserVersion = v1.0.0
  Vendor = Zeek
  Product = Zeek
  TimeFormat = "epoch_sec"
  Conditions = [ """/smtp.log""" ]
  Fields = [
    """({time}\d{10})\.\d{6}\s+({alert_id}[^\s]+)\s+(?:-|(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|[^\s]+))\s+(?:-|(({src_port}\d+?)|[^\s]+))\s+(?:-|(({dest_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|[^\s]+))\s+(?:-|(({dest_port}\d+?)|[^\s]+))\s+(?:-|({trans_depth}[^\s]+))\s+(?:-|({helo}[^\s]+))\s+(?:-|({mailfrom}[^\s]+))\s+(?:-|({rcptto}[^\s]+))\s+(?:-|([^\s]+))\s+(?:-|([^\s]+))\s+(?:-|([^\s]+))\s+((?:-|({cc}[^\s]+))\s+)?(?:-|({reply_to}[^\s]+))\s+(?:-|(<)?({message_id}.+?)(>)?)\s+(?:-|({in_reply_to}[^\s]+))\s+(?:-|({email_subject}[^\s]+))\s+(?:-|([^\s]+))\s+(?:-|([^\s]+))\s+(?:-|([^\s]+))\s+(?:-|([^\s]+))\s+(?:-|({path}[^\s]+))\s(?:-|({user_agent}[^\s]+))\s+(?:-|({tls}[^\s]+))\s+(?:-|\((empty)\)|({email_attachments}[^\s]+))\s+(?:-|([^\s]+?))\s*""",
    """\d{10}\.\d{6}\s([^\s]+\s+){7}({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\s""",
    """\d{10}\.\d{6}\s([^\s]+\s+){8}({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """\d{10}\.\d{6}\s([^\s]+\s+){20}({result_code}\d+)\s+({result}.+?)[\s*\t|\s*\[]((\[InternalId=({alert_id}\d+),\s*Hostname=({dest_host}[^\]]+)\]))?"""
  ]


}
```