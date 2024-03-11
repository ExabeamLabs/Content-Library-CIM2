#### Parser Content
```Java
{
Name = mcafee-dlp-cef-file-write-success-blockusb
    Vendor = McAfee
    Product = McAfee ePolicy Orchestrator
    TimeFormat = "epoch"
    Conditions = [ """CEF:""", """|McAfee|ePolicy""", """|Threat:""" ]
    Fields = [ """\srt=({time}\d{13})""",
      """\sdvchost=({host}[^\s]+)""",
      """\sexternalId=({alert_id}\d+)""",
      """CEF([^\|]*\|){5}({alert_name}[^|]+)""",
      """CEF([^\|]*\|){6}({alert_severity}[^|]+)""",
      """\smsg=({alert_type}[^=]+?)\s+\w+=""",
      """\smsg=({operation_details}[^=]+?)\s+\w+=""",
      """\smsg=[^=]+?(MONITOR|, PERMITTED)\s+({device_type}[^=]+?)\s+\w+=""",
      """\sshost=({dest_host}[^\s]+)""",
      """\ssrc=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """\ssuser=(({domain}[^\\]+)\\+)?({user}[^=]+?)\s+\w+="""
    ]
	ParserVersion = "v1.0.0"
  

}
```