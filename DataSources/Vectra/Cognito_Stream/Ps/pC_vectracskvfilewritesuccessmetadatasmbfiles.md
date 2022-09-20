#### Parser Content
```Java
{
Name = vectra-cs-kv-file-write-success-metadatasmbfiles
  TimeFormat = "epoch_sec"
  Conditions = [ """COGNITO_STREAM""", """vectra_metadata_smbfiles""", """action="SMB::FILE_""", """METADATA_SMBFILES""" ]
  Fields = ${VectraParserTemplates.vectra-meta-data.Fields} [
    """action="SMB::FILE_({access}[^"]+)"""",
    """path="({src_file_path}[^"]+)"""",
    """\sname="({src_file_path}(({file_dir}[^"]*?)\\+)?({src_file_name}[^"\\\.]+?(\.({src_file_ext}[^"\.\\]+))?))""""
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