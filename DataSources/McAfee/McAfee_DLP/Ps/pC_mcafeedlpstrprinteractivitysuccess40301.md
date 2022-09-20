#### Parser Content
```Java
{
Name = mcafee-dlp-str-printer-activity-success-40301
  Vendor = McAfee
  Product = McAfee DLP
  TimeFormat = "epoch_sec"
  Conditions = [ """|Log Email Printing|""", """|40301|""" ]
  Fields = [
     """^([^|]*\|){29}({app}[^|]+)""",
     """^([^|]*\|){14}({dest_ip}[a-fA-F:\d.]+)""",
     """^([^|]*\|){12}({event_name}[^|]+)""",
     """^([^|]*\|){15}({host}[^|]+)""",
     """^([^|]*\|){17}({object}[^|]+)""",
     """^([^|]*\|){11}({printer_name}[^|]+)""",
     """^([^|]*\|){2}({time}[^|]+)""",
     """^([^|]*\|){20}(({domain}[^\\]+)\\*)?({user}[^|]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```