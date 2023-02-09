#### Parser Content
```Java
{
Name = unix-sm-str-email-virusclean
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix Sendmail
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [
"""AntiVirus:""",
""" classification="""
  ]
  Fields = [
    """\d{2}:\d{2}:\d{2} ({host}[\w.\-]+) \S+ \[.+?\-({alert_id}\w+)\]""",
    """({av_vendor}\S+)\.AntiVirus:""",
    """\sclassification=({malware_score}[^,]+)""",
  ]


}
```