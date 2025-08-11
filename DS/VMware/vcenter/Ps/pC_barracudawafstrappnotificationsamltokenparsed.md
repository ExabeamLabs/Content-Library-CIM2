#### Parser Content
```Java
{
Name = barracuda-waf-str-app-notification-samltokenparsed
  ParserVersion = v1.0.0
  Vendor = VMware
  Product = vCenter
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """SAML token for """, """ successfully parsed from""" ]
  Fields = [
    """({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d+Z)"""
    """({additional_info}SAML token for .*)""",
  ]


}
```