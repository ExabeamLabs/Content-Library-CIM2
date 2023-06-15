#### Parser Content
```Java
{
Name = mcafee-es-cef-file-write-success-deviceplug
    Vendor = McAfee
    Product = McAfee Endpoint Security
    TimeFormat = "epoch"
    Conditions = [ """|McAfee|Host Data Loss Prevention|""", """|DEVICE_PLUG|""" ]
    Fields = [
        """\srt=({time}\d{13})""",
        """\sdhost=({dest_host}.+?)\s\w+=""",
        """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s\w+=""",
        """\sduser=(({domain}[^\\]+)\\+)?({user}[^=]+)\s\w+=""",
        """\scs4=([^,]*,){4}\s*({device_id}.+?)(\s\w+=|&\d|,)""",
        """\scs4=([^,]*,)\s*({device_type}[^,]+)""",
        """\scs4=([^,]*,\s*){2}({operation_details}[^,]+)""",
        """\|McAfee\|Host Data Loss Prevention\|([^|]*\|)({operation}[^|]+)""",
    ]
	ParserVersion = "v1.0.0"
  

}
```