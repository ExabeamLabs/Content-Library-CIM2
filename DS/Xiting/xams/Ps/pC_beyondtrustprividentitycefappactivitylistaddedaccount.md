#### Parser Content
```Java
{
Name = "beyondtrust-prividentity-cef-app-activity-listaddedaccount"
Conditions = [
  """CEF:"""
  """|Liebsoft|"""
  """|EVENT_ID_SHARED_CREDENTIAL_LIST_ADDED_ACCOUNT|"""
]
ParserVersion = "v1.0.0"

vectra-meta-data.Fields} [
    """result_code="(noSuchObject|({result}[^"]+))""""
  ]
  ParserVersion = "v1.0.0"
},

${VectraParserTemplates.vectra-meta-data}{
  Name = vectra-cs-kv-email-send-success-metadatasmtp
  TimeFormat = "epoch"
  Conditions = [ """COGNITO_STREAM""", """vectra_metadata_smtp""", """METADATA_SMTP""" ]
  Fields = ${VectraParserTemplates.vectra-meta-data.Fields} [
    """subject="({log_subject}[^"]+)"""",
    """mail_from="({src_email_address}[^"@]+@[^"]+)"""",
    """rcpt_to="({dest_email_address}[^"@]+@[^"]+)"""",
    """msgid="<({message_id}[^"]+)>""""
  ]
  ParserVersion = "v1.0.0"
},

${VectraParserTemplates.vectra-meta-data}{
  Name = vectra-cs-kv-file-write-success-metadatasmbfiles
  TimeFormat = "epoch"
  Conditions = [ """COGNITO_STREAM""", """vectra_metadata_smbfiles""", """action="SMB::FILE_""", """METADATA_SMBFILES""" ]
  Fields = ${VectraParserTemplates.vectra-meta-data.Fields} [
    """action="SMB::FILE_({access}[^"]+)"""",
    """path="({file_path}[^"]+)"""",
    """\sname="({file_path}(({file_dir}[^"]*?)\\+)?({file_name}[^"\\\.]+?(\.({file_ext}[^"\.\\]+))?))""""
  ]
  ParserVersion = "v1.0.0"
},

${VectraParserTemplates.vectra-meta-data}{
  Name = vectra-cs-kv-endpoint-login-success-metadatantlm
  TimeFormat = "epoch"
  Conditions = [ """COGNITO_STREAM""", """vectra_metadata_ntlm""", """METADATA_NTLM""" ]
  Fields = ${VectraParserTemplates.vectra-meta-data.Fields} [
    """username="({user}[\w\.\-]{1,40}\$?)"""",
    """domain="({domain}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"
},

${VectraParserTemplates.vectra-meta-data}{
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
}

{
  Name = xiting-x-cef-app-login-success-erfolgreich
  Vendor = Xiting
  Product = XAMS
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """Login erfolgreich""", """CEF:""", """|Xiting|XAMS|""", """"USERID":"""" ]
  Fields = [
    """"USERID":"({user}[\w\.\-]{1,40}\$?)"""",
    """({app}XAMS)""",
    """({event_name}Login erfolgreich)"""
    """"MSG":"({additional_info}[^"]+)""""
  
}
```