#### Parser Content
```Java
{
Name = mcafee-dlp-cef-alert-trigger-success-deviceplug
    Vendor = McAfee
    Product = McAfee DLP
    TimeFormat = "epoch"
    Conditions = [ """|McAfee|Host Data Loss Prevention|""", """|DEVICE_PLUG|""", """Block,""" ]
    Fields = [
        """\srt=({time}\d+)""",
        """\sdhost=({src_host}.+?)\s\w+=""",
        """\sdst=({src_ip}.+?)\s\w+=""",
        """\sduser=(({domain}[^\\]+)\\+)?({user}[^=]+)\s\w+=""",
        """\sact=({alert_type}.+?)\s\w+=""",
        """\scs1=({alert_name}.+?)(,|\s\w+=)""",
        """\scs4=([^,]*,){4}\s*({device_id}.+?)(\s\w+=|&\d|,)""",
        """\scs4=([^,]*,)\s*({device_type}[^,]+)""",
        """\|McAfee\|Host Data Loss Prevention\|([^|]*\|){2}({additional_info}[^|]+)"""
    ]
    ParserVersion = "v1.0.0"
  

}
```