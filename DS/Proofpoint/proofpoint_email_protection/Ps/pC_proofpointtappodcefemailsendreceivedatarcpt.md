#### Parser Content
```Java
{
Name = proofpoint-tappod-cef-email-send-receive-datarcpt
  ParserVersion = v1.0.0
  Vendor = Proofpoint
  Product = Proofpoint Email Protection
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","MMM dd HH:mm:ss"]
  Conditions = [
"""mod=session cmd=data rcpt="""
  ]
  Fields = [
    """"+host"+:"+({host}[^"]+)""",
    """({time}\w{3}\s+\d+\s\d\d:\d\d:\d\d)\s({host}[\w\-\.]+)\s""",
    """"@timestamp"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"+"""
    """\sx=({alert_id}.+?)\s+(\w+=|$)""",
    """\srcpt=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\s+(\w+=|$)"""
  ]


}
```