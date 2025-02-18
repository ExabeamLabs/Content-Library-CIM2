#### Parser Content
```Java
{
Name = microsoft-defenderep-kv-alert-trigger-success-systemcenterep
  Vendor = Microsoft
  Product = Microsoft Defender
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """"SystemCenterEndpointProtection"""" ]
  Fields = [
    """\sdest_name="+({src_host}[^\s"]+)""",
    """(Timestamp: |Timestamp=)"+({time}\d+-\d+-\d+ \d\d:\d\d:\d\d)""",
    """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """((?i)RowID)"?:\s*"+({alert_id}[^"]+)""",
    """((?i)TargetHost)"?:\s*"+({dest_host}[\w\-.]+)""",
    """((?i)TargetUser"?:\s*|user=)"+(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """((?i)TargetResource)"?:\s*"+({additional_info}[^"]+)""",
    """((?i)ClassificationType"?:\s*|signature=)"+({alert_name}[^"]+)""",
    """((?i)ClassificationSeverity"?:\s*|severity=)"+({alert_severity}[^"]+)""",
    """((?i)ClassificationCategory"?:\s*|category=)"+({alert_type}[^"]+)""",
    """\sfile_path="+({malware_url}[^",]+)""",
    """(SrcAddress: |src=)"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """((?i)TargetProcess)"?(:|=)\s*"+({process_path}[^"]+\\({process_name}[^"]+))""",
  ]
  ParserVersion = "v1.0.0"


}
```