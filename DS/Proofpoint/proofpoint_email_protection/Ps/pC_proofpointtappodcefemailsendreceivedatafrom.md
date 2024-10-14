#### Parser Content
```Java
{
Name = proofpoint-tappod-cef-email-send-receive-datafrom
  ParserVersion = v1.0.0
  Vendor = Proofpoint
  Product = Proofpoint Email Protection
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [
"""mod=session cmd=data from="""
  ]
  Fields = [
    """"+host"+:"+({host}[^"]+)""",
    """"@timestamp"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"+"""
    """\sx=({alert_id}.+?)\s+(\w+=|$)""",
    """\sfrom=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\s+(\w+=|$)"""
  ]


}
```