#### Parser Content
```Java
{
Name = symantec-dlp-kv-alert-trigger-success-blocked
  ParserVersion = v1.0.0
  Vendor = Symantec
  Product = Symantec DLP
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """Policy Violated: """, """Endpoint: """, """Blocked: """ ]
  Fields = [
    """\s({host}[^.\s]+)(\.\w+)*\s*(Message =)? ID:\s({alert_id}\d+)""",
    """\WPolicy Violated: ({alert_name}.+?)(,\s*\w+:|\s*$)""",
    """\WProtocol:\s+({alert_type}.+?)(,\s*\w+:|\s*$)""",
    """\WProtocol:\s+({protocol}.+?)(,\s*\w+:|\s*$)""",
    """\WRecipient:\s+(?:N\/A|({target}.+?))(,\s*\w+:|\s*$)""",
    """\WRecipient:\s+({account}[^@]+)@({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\WSender:\s+(?:N\/A|({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({user}[^@,]+))""",
    """\WSender:\s+({os}[^:]+):\/+({domain}[^/]+)\/({user}[^,]+)""",
    """\WSeverity:\s+({alert_severity}.+?)(,\s*\w+:|\s*$)""",
    """\sPATH:\s+(|({file_path}({file_dir}.*?[\\\/,]+)?({file_name}[^\\\/,]+?(\.({file_ext}\w+))?)))(,\s*\w+:|\s*$)""",
    """\WFilename:\s+(?:N\/A|({file_name}.+?))(,\s*\w+:|\s*$)""",
    """\WProtocol: FTP,.+?Subject:\s+(FTP\s+)?({src_file_name}.+?)\s*(\(|,)""",
    """\WProtocol: FTP,.+?Subject:.+?\(({bytes}\d+)""",
    """\WEndpoint:\s+(?:N\/A|({src_host}.+?))(,\s*\w+:|\s*$|\s*"|\s+\w+=)""",
    """\WBlocked:\s+({action}[^,]+?(,User:[^:]+?)?)(,\s*\w+:|\s*$)""",
    """ViolatorsName:\s+(({full_name}\w+(,\s*\w+)+)|({user}\w+))(,\s*\w+:|\s*$)""",
    """ViolatorsUserID:\s+({user_id}[^,]+)(,\s*\w+:|\s*$)""",
    """ViolatorsEmail:\s+({email_address}[^@\s]+@[^\s,]+)(,\s*\w+:|\s*$)""",
    """\sDEVICE_ID:\s+({device_id}[^,]+)(,\s*\w+:|\s*$)""",
    """\sApplication_name:\s+({process_name}[^,]+)(,\s*\w+:|\s*$)""",
    """\WSubject:\s+({email_subject}[^,]+?)(,\s*\w+:|\s*$)""",
    """\WAttachment_Filename:\s+({email_attachments}[^,]+?)(,\s*\w+:|\s*$)"""
  ]
  DupFields = ["email_address->src_email_address", "target->email_recipients"]
  SOAR {
    IncidentType = "dlp"
    DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "user->dlpUser", "alert_name->dlpPolicy", "alert_severity->sourceSeverity", "protocol->dlpProtocol", "src_host->dlpDeviceName", "src_file_name->dlpFileName", "bytes->dlpFileSize", "action->dlpActionTaken"]
    NameTemplate = """Vontu DLP Alert ${alert_name} found"""
    ProjectName = "SOC"
    EntityFields = [
      {EntityType="device", Name ="src_address", Fields=["src_ip->ip_address", "src_host->host_name"]

}
```