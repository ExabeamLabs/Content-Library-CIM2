#### Parser Content
```Java
{
Name = forcepoint-ngfw-cef-network-traffic-success-connectionallowed
  ParserVersion = v1.0.0
  Product = Forcepoint Next-Gen Firewall
  Conditions = [ """CEF:""", """|FORCEPOINT|""", """|Connection_Allowed|""" ]
  Fields = ${ForcepointParsersTemplates.forcepoint-template.Fields} [
    """proto=\s*({protocol}.+?)(\s\w+=)""",
    ]


}
```