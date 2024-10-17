#### Parser Content
```Java
{
Name = mcafee-dlp-str-printer-activity-success-40301
  Vendor = McAfee
  Product = McAfee DLP Endpoint
  TimeFormat = "epoch_sec"
  Conditions = [ """|Log Email Printing|""", """|40301|""" ]
  Fields = [
     """^([^|]*\|){29}({app}[^|]+)""",
     """^([^|]*\|){14}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
     """^([^|]*\|){12}({event_name}[^|]+)""",
     """^([^|]*\|){15}({host}[^|]+)""",
     """^([^|]*\|){17}({object}[^|]+)""",
     """^([^|]*\|){11}({printer_name}[^|]+)""",
     """^([^|]*\|){2}({time}\d{10})\.\d{3}""",
     """^([^|]*\|){20}(({domain}[^\\]+)\\*)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  ]
  ParserVersion = "v1.0.0"


}
```