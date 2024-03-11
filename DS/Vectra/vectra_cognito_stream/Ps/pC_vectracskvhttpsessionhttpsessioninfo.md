#### Parser Content
```Java
{
Name = vectra-cs-kv-http-session-httpsessioninfo
  TimeFormat = "epoch"
  Conditions = [ """COGNITO_STREAM""", """vectra_metadata_httpsessioninfo""", """METADATA_HTTPSESSIONINFO""" ]
  Fields = ${VectraParserTemplates.vectra-meta-data.Fields} [
    """method="({method}[^"]+)"""",
    """orig_ip_bytes="({bytes_in}\d+)"""",
    """resp_ip_bytes="({bytes_out}\d+)"""",
    """status_code="({http_response_code}\d+)"""",
    """user_agent="({user_agent}[^"]+)"""",
    """uri="({web_domain}[^:\/"]+)?(:\d+)?({uri_path}\/[^"\?]+)?({uri_query}\?[^"]+)?""""
  ]
  ParserVersion = "v1.0.0"

vectra-meta-data = {
  Vendor = Vectra
  Product = Vectra Cognito Stream
  TimeFormat = "epoch"
  Fields = [
    """\sts="+({time}\d{13})""",
    """id.orig_h="+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"+"""
    """id.orig_p="+({src_port}\d+)"+""",
    """id.resp_h="+({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"+""",
    """id.resp_p="+({dest_port}\d+)"+""",
    """orig_hostname="+(null|((IP-)*((\d+\.){3}\d+|([A-Fa-f0-9]+:[A-Fa-f0-9:]+)|({src_host}[^"]+))))""""
    """resp_hostname="+(null|((IP-)*((\d+\.){3}\d+|([A-Fa-f0-9]+:[A-Fa-f0-9:]+)|({dest_host}[^"]+))))""""
  ]
 
}
```