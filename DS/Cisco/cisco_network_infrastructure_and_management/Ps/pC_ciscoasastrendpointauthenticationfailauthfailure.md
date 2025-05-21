#### Parser Content
```Java
{
Name = cisco-asa-str-endpoint-authentication-fail-authfailure
  Vendor = Cisco
  Product = Cisco Network Infrastructure and Management
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  ParserVersion = "v1.0.0"
  Conditions = ["""Authentication failure for SNMP""", """SNMP-3-AUTHFAIL"""]
  Fields = [
    """host\s(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({src_port}\d+))?|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))""",
    """Source:\s\/(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({dest_port}\d+))?|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))""",
    """AUTHFAIL:\s({event_name}.*?)\sfrom""",
    """UTC:\s({event_code}.*?):"""
  ]
   DupFields = [ "dest_ip->host" ]


}
```