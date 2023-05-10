#### Parser Content
```Java
{
Name = nozomi-guardian-cef-alert-trigger-success-n2os
    Vendor = Nozomi Networks
    Product = Guardian
    ParserVersion = "v1.0.0"
    TimeFormat = "epoch"
    Conditions = ["""CEF:""", """|Nozomi Networks|""", """|N2OS|""", """flexString3="""]
    Fields = [
      """\sdvchost=({host}[\w.-]+)""",
      """\scs1=({alert_severity}[^\s]+)""",
      """\|Nozomi Networks\|([^\|]+\|){2}({alert_type}[^\|]+)""",
      """\scs3=({alert_id}[^\s]+)""",
      """\ssrc=({src_ip}[a-fA-F\d.:]+)\s""",
      """\sspt=({src_port}\d+)""",
      """\sdpt=({dest_port}\d+)""",
      """\sflexString3=({alert_name}.+?)(?=(?:\s|\||,|;)[\w.-]+=)""",
      """\s\WMD5:\s({hash_md5}[^)\s]+)""",
      """\smsg=({additional_info}.+?)(?=(?:\s|\||,|;)[\w.-]+=)""",
      """\sshost=({src_host}[\w.-]+)""",
      """\sflexString1=({mitre_tech}[^\s]+)""",
      """\sflexString2=({mitre_tactic}[^\s]+)""",
      """\sstart=({time}\d{13})""",
      """\sproto=((?i)UNKNOWN|({protocol}[^\s]+))""",
      """\sdst=({dest_ip}[a-fA-F\d.:]+)""",
      """\sdhost=({dest_host}[\w.-]+)""",
      """\Sapp=({app}[^\s]+)"""
  ]


}
```