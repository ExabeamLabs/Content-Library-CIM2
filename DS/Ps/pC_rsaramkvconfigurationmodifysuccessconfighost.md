#### Parser Content
```Java
{
Name = rsa-ram-kv-configuration-modify-success-confighost
  Conditions = [ """ SINGLEPOINT """, """ SYSTEM_CONFIG_HOST """ ]
  Fields = ${DLRSAParserTemplate.rsa-system-events.Fields}[
    """HOST_IP="({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """ALIASES="({host}[\w\.\-]+)"""",
    """\]\s+({additional_info}[^"]+?)\.*\s*$"""
  ]
  ParserVersion = "v1.0.0"


}
```