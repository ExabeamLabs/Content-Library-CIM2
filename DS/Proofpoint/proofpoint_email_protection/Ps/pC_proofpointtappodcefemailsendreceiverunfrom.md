#### Parser Content
```Java
{
Name = proofpoint-tappod-cef-email-send-receive-runfrom
  ParserVersion = v1.0.0
  Vendor = Proofpoint
  Product = Proofpoint Email Protection
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [
"""mod=dmarc cmd=run""",
"""header.from"""
  ]
  Fields = [
    """"+host"+:"+({host}[^"]+)""",
    """"@timestamp"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"+"""
    """\sx=({alert_id}.+?)\s+(\w+=|$)""",
    """\sheader.from=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  ]


}
```