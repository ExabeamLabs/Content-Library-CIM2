#### Parser Content
```Java
{
Name = proofpoint-tappod-cef-email-send-receive-run
  ParserVersion = v1.0.0
  Vendor = Proofpoint
  Product = Proofpoint TAP/POD
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [
"""mod=spam cmd=run rule="""
  ]
  Fields = [
    """"+host"+:"+({host}[^"]+)""",
    """"@timestamp"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"+"""
    """\sx=({xid}.+?)\s+(\w+=|$)""",
    """\smalwarescore=({malware_score}[^=]+?)\s+(\w+=|$)""",
    """\sphishscore=({phishing_score}[^=]+?)\s+(\w+=|$)""",
    """\sspamscore=({spam_score}[^=]+?)\s+(\w+=|$)""",
    """\sadultscore=({spam_score}[^=]+?)\s+(\w+=|$)"""
  ]


}
```