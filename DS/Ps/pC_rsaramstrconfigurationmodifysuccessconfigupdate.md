#### Parser Content
```Java
{
Name = rsa-ram-str-configuration-modify-success-configupdate
  Conditions = [ """ SINGLEPOINT """, """ SYSTEM_CONFIG_UPDATE """ ]
  Fields = ${DLRSAParserTemplate.rsa-system-events.Fields}[
    """\]\s+({additional_info}[^"]+?)\.*\s*$"""
  ]
  ParserVersion = "v1.0.0"


}
```