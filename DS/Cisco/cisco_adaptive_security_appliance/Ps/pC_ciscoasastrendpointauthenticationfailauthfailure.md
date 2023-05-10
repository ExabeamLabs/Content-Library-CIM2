#### Parser Content
```Java
{
Name = cisco-asa-str-endpoint-authentication-fail-authfailure
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  ParserVersion = "v1.0.0"
  Conditions = ["""Authentication failure for SNMP""", """SNMP-3-AUTHFAIL"""]
  Fields = [
    """host\s(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))""",
    """Source:\s\/(({dest_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))""",
    """AUTHFAIL:\s({event_name}.*?)\sfrom""",
    """UTC:\s({event_code}.*?):"""
  ]
   DupFields = [ "dest_ip->host" ]


}
```