#### Parser Content
```Java
{
Name = cyberark-vault-kv-app-activity-auditrecord
  ParserVersion = v1.0.0
  Vendor = CyberArk
  Product = CyberArk Vault
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """CyberArk Vault - Audit Record""", """ act=""", """ sourceip=""", """ reason=""", """ cs2=""" ]
  Fields = [
    """({app}CyberArk Vault)""",
    """({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d(\+|-)\d\d:\d\d)\s({host}[\w\-.]+)\s""",
    """({record_type}Audit Record)""",
    """\sact="({operation}[^"=]+)"""",
    """\ssuser="(-|({user}[^"=]+))"""",
    """\sfname="(-|({file_path}({file_dir}[^"=]*?[\\\/]+)?({file_name}[^"=\\\/]+?(\.({file_ext}\w+))?)))"""",
    """\ssourceip="({src_ip}[A-Fa-f\d:.]+)"""",
    """\sshost="(-|0\.0\.0\.0|(({src_ip}(\d{1,3}\.){3}\d{1,3})|({src_host}[^"=]+)))"""",
    """\sdhost="(-|0\.0\.0\.0|(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[^"=]+)))"""",
    """\sduser="(-|({dest_user}[^"=]+))"""",
    """\sreason="(-|({failure_reason}[^"=]+))"""",
    """\scs2="(-|({safe_name}[^"=]+))"""",
    """\scs3="(-|({device_type}[^"=]+))"""",
    """\scs4="(-|({db_name}[^"=]+))"""",
    """\smsg="(-|({additional_info}[^"]+?))\s*""""
  ]
  DupFields=[ "operation->event_name", "file_path->object" ]


}
```