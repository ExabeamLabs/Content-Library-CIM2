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
    """ts="+({time}\d{13})""",
    """id.orig_h="+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"+"""
    """id.orig_p="+({src_port}\d+)"+""",
    """id.resp_h="+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"+""",
    """id.resp_p="+({dest_port}\d+)"+""",
    """orig_hostname="+({src_host}[^"]+)"+"""
    """resp_hostname="+(null|((IP-)*({dest_host}[^"]+)))""",
    """result_code="+({result}[^"]+)"+""",
    """uid="*({user}[^"\s]+)"""
  ]


}
```