#### Parser Content
```Java
{
Name = rsa-ram-str-configuration-routing-modify-success-systemconfig
  Conditions = [ """ SINGLEPOINT """, """ SYSTEM_CONFIG_ROUTE """ ]
  Fields = ${DLRSAParserTemplate.rsa-system-events.Fields}[
    """RULE="({rule}[^"]+)"""",
    """\]\s+({additional_info}[^"]+?)\.*\s*$"""
  ]
  ParserVersion = "v1.0.0"


}
```