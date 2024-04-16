#### Parser Content
```Java
{
Name = semperis-dsp-kv-endpoint-notification-success-indicatorfound
  Vendor = Semperis
  Product = Semperis DSP
  ParserVersion = v1.0.0
  TimeFormat = "dd/MMM/yyyy HH:mm:ss.SSSS"
  Conditions = [  """Security indicator found:""", """Result: """, """Forest name:""" ]
  Fields = [
    """({event_name}Security indicator found)""",
    """Result:\s*({result}[\S]+)""",
    """Domains:\s*({domain}[^:]+?)\s\w+?:""",
    """Severity:\s*({alert_severity}[^:]+?)\s\w+?:""",
    """Security indicator found:\s*({additional_info}[^:]+?)\s+Generation time:"""
  ]


}
```