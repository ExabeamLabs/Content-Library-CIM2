#### Parser Content
```Java
{
Name = cyberark-pam-kv-app-activity-auditrecord
  ParserVersion = v1.0.0
  Vendor = CyberArk
  Product = "CyberArk Privilege Access Manager"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """CyberArk Vault - Audit Record""", """ act=""", """ sourceip=""", """ reason=""", """ cs2=""" ]
  Fields = [
    """({app}CyberArk Vault)""",
    """({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d(\+|-)\d\d:\d\d)\s({host}[\w\-.]+)\s""",
    """({record_type}Audit Record)""",
    """\sact="({operation}[^"=]+)"""",
    """\ssuser="(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """\sfname="(-|({file_path}({file_dir}[^"=]*?[\\\/]+)?({file_name}[^"=\\\/]+?(\.({file_ext}\w+))?)))"""",
    """\ssourceip="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """\sshost="(-|0\.0\.0\.0|(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({src_host}[^"=]+)))"""",
    """\sdhost="(-|0\.0\.0\.0|(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[^"=]+)))"""",
    """\sduser="(-|({dest_user}[^"=]+))"""",
    """\sreason="(-|({result_reason}[^"=]+))"""",
    """\scs2="(-|({safe_name}[^"=]+))"""",
    """\scs3="(-|({device_type}[^"=]+))"""",
    """\scs4="(-|({db_name}[^"=]+))"""",
    """\smsg="(-|({additional_info}[^"]+?))\s*""""
  ]
  DupFields=[ "operation->event_name", "file_path->object" ]


}
```