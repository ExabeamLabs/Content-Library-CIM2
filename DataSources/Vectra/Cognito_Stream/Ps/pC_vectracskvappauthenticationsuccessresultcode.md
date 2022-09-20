#### Parser Content
```Java
{
Name = vectra-cs-kv-app-authentication-success-resultcode
  TimeFormat = "epoch_sec"
  Conditions = [ """COGNITO_STREAM""", """vectra_metadata_ldap""", """METADATA_LDAP""", """result_code="""" ]
  Fields = ${VectraParserTemplates.vectra-meta-data.Fields} [
    """result_code="(noSuchObject|({result}[^"]+))""""
  ]
  ParserVersion = "v1.0.0"

vectra-meta-data = {
  Vendor = Vectra
  Product = Cognito Stream
  TimeFormat = "epoch"
  Fields = [
    """\sts="+({time}\d+)""",
    """id.orig_h="+({src_ip}\d+.\d+.\d+.\d+)"+"""
    """id.orig_p="+({src_port}\d+)"+""",
    """id.resp_h="+({dest_ip}\d+.\d+.\d+.\d+)"+""",
    """id.resp_p="+({dest_port}\d+)"+""",
    """orig_hostname="+(null|((IP-)*((\d+\.){3}\d+|([A-Fa-f0-9]+:[A-Fa-f0-9:]+)|({src_host}[^"]+))))""""
    """resp_hostname="+(null|((IP-)*((\d+\.){3}\d+|([A-Fa-f0-9]+:[A-Fa-f0-9:]+)|({dest_host}[^"]+))))""""
  ]
 
}
```