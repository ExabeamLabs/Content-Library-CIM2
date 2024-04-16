#### Parser Content
```Java
{
Name = cofense-pm-cef-alert-trigger-success-rulematch
  Vendor = Cofense
  Product = Cofense Phishme
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """CEF:""", """|Cofense|Triage|""", """|Rule Match|""" ]
  Fields = [
    """({alert_type}Rule Match)""",
    """\Wrt=({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d)""",
    """\Wduser=(|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))(\s+\w+=|\s*$)""",
    """\Wsuser=(|({malware_url}.+?))(\s+\w+=|\s*$)""",
    """\Wcs2=(|({alert_name}.+?))(\s+\w+=|\s*$)""",
    """\Wcs4=(|({additional_info}.+?))(\s+\w+=|\s*$)""",
  ]
  ParserVersion = "v1.0.0"


}
```