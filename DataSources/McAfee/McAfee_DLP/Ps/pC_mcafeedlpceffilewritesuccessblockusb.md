#### Parser Content
```Java
{
Name = mcafee-dlp-cef-file-write-success-blockusb
    Vendor = McAfee
    Product = McAfee DLP
    TimeFormat = "epoch"
    Conditions = [ """CEF:""", """|McAfee|ePolicy""", """|Threat:""" ]
    Fields = [ """\srt=({time}\d+)""",
      """\sdvchost=({host}[^\s]+)""",
      """\sexternalId=({alert_id}\d+)""",
      """CEF([^\|]*\|){5}({alert_name}[^|]+)""",
      """CEF([^\|]*\|){6}({alert_severity}[^|]+)""",
      """\smsg=({alert_type}[^=]+?)\s+\w+=""",
      """\smsg=({activity_details}[^=]+?)\s+\w+=""",
      """\smsg=[^=]+?(MONITOR|, PERMITTED)\s+({device_type}[^=]+?)\s+\w+=""",
      """\sshost=({dest_host}[^\s]+)""",
      """\ssrc=({dest_ip}[A-Fa-f:\d.]+)""",
      """\ssuser=(({domain}[^\\]+)\\+)?({user}[^=]+?)\s+\w+="""
    ]
	ParserVersion = "v1.0.0"
  

}
```