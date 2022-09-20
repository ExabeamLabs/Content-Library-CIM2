#### Parser Content
```Java
{
Name = vectra-cs-kv-network-session-success-ldap
  Vendor = Vectra
  Product = Vectra Cognito Stream
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch"
  Conditions = [ """vectra_metadata_ldap""", """METADATA_LDAP""" ]
  Fields = [
    """ts="+({time}\d+)""",
    """id.orig_h="+({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})"+"""
    """id.orig_p="+({src_port}\d+)"+""",
    """id.resp_h="+({dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})"+""",
    """id.resp_p="+({dest_port}\d+)"+""",
    """orig_hostname="+({src_host}[^"]+)"+"""
    """resp_hostname="+(null|((IP-)*({dest_host}[^"]+)))""",
    """result_code="+({result}[^"]+)"+""",
    """uid="*({user}[^"\s]+)"""
  ]


}
```