#### Parser Content
```Java
{
Name = semperis-dsp-kv-user-privilege-use-success-permissionchanges
  Vendor = Semperis
  Product = Semperis DSP
  TimeFormat = "dd/MMM/yyyy HH:mm:ss.SSSS"
  Conditions = [  """Security indicator passed:""", """Permission changes""", """Result: """, """Forest name:""" ]
  Fields = [
    """({event_name}Permission changes)""",
    """Permission changes on ({object}[^:]+?) object""",
    """Result:\s*({result}[\S]+)""",
    """Domains:\s*({domain}[^:]+?)\s\w+?:""",
    """Severity:\s*({alert_severity}[^:]+?)\s\w+?:""",
    """Security indicator passed:\s*({additional_info}[^:]+?)\s+Generation time:"""
  ]
  ParserVersion = "v1.0.0"


}
```