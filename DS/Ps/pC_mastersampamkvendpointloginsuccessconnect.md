#### Parser Content
```Java
{
Name = "mastersam-pam-kv-endpoint-login-success-connect"
Conditions = [
  """ Activity:connect """
]
ParserVersion = "v1.0.0"

tippingpoint-sms-alert-template.Fields} [
    """00000001-0001-0001-0001-00000\d+\s+.+?\s+\d+\s+({protocol}http)""",
    """00000001-0001-0001-0001-00000\d+\s+.+?\s+\d+\s+http(\s+[^\s]+){4}\s+({hit_cnt}\d+)\s+""",
    """00000001-0001-0001-0001-00000\d+\s+.+?\s+\d+\s+http(\s+[^\s]+){5}\s+({src_zone_name}[^\s]+)\s+({dest_zone}[^\s]+)""",
    """00000001-0001-0001-0001-00000\d+\s+.+?\s+\d+\s+http(\s+[^\s]+){8}\s+({vlan_id}\d+)""",
    """00000001-0001-0001-0001-00000\d+\s+.+?\s+\d+\s+http(\s+[^\s]+){9}\s+({host}[^\s]+)""",
    """00000001-0001-0001-0001-00000\d+\s+.+?\s+\d+\s+http(\s+[^\s]+){11}\s+({time}\d{13})""",
    """00000001-0001-0001-0001-00000\d+\s+.+?\s+\d+\s+http(\s+[^\s]+){12}\s+({alert_id}\d+)""",
    """http\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s+({src_port}\d+)\s+({dest_ip}[a-fA-F\d.:]+)\s+({dest_port}\d+)"""
  
}
```