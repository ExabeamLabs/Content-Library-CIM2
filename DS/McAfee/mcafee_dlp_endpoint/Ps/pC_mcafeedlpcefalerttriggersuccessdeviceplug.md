#### Parser Content
```Java
{
Name = mcafee-dlp-cef-alert-trigger-success-deviceplug
    Vendor = McAfee
    Product = McAfee DLP Endpoint
    TimeFormat = "epoch"
    Conditions = [ """|McAfee|Host Data Loss Prevention|""", """|DEVICE_PLUG|""", """Block,""" ]
    Fields = [
        """\srt=({time}\d{13})""",
        """\sdhost=({src_host}.+?)\s\w+=""",
        """\sdst=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s\w+=""",
        """\sduser=(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s\w+=""",
        """\sact=({alert_type}.+?)\s\w+=""",
        """\scs1=({alert_name}.+?)(,|\s\w+=)""",
        """\scs4=([^,]*,){4}\s*({device_id}.+?)(\s\w+=|&\d|,)""",
        """\scs4=([^,]*,)\s*({device_type}[^,]+)""",
        """\|McAfee\|Host Data Loss Prevention\|([^|]*\|){2}({additional_info}[^|]+)"""
    ]
    ParserVersion = "v1.0.0"
  

}
```