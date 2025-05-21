#### Parser Content
```Java
{
Name = vectra-cs-kv-file-write-success-metadatasmbfiles
  TimeFormat = "epoch"
  Conditions = [ """COGNITO_STREAM""", """vectra_metadata_smbfiles""", """action="SMB::FILE_""", """METADATA_SMBFILES""" ]
  Fields = ${VectraParserTemplates.vectra-meta-data.Fields} [
    """action="SMB::FILE_({access}[^"]+)"""",
    """path="({file_path}[^"]+)"""",
    """\sname="({file_path}(({file_dir}[^"]*?)\\+)?({file_name}[^"\\\.]+?(\.({file_ext}[^"\.\\]+))?))""""
  ]
  ParserVersion = "v1.0.0"

vectra-meta-data = {
  Vendor = Vectra
  Product = Vectra Cognito Stream
  TimeFormat = "epoch"
  Fields = [
    """\sts="+({time}\d{13})""",
    """id.orig_h="+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"+"""
    """id.orig_p="+({src_port}\d+)"+""",
    """id.resp_h="+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"+""",
    """id.resp_p="+({dest_port}\d+)"+""",
    """orig_hostname="+(null|((IP-)*((\d+\.){3}\d+|([A-Fa-f0-9]+:[A-Fa-f0-9:]+)|({src_host}[^"]+))))""""
    """resp_hostname="+(null|((IP-)*((\d+\.){3}\d+|([A-Fa-f0-9]+:[A-Fa-f0-9:]+)|({dest_host}[^"]+))))""""
  ]
 
}
```