#### Parser Content
```Java
{
Name = mcafee-es-str-file-write-success-usbconditions
    Vendor = McAfee
    Product = McAfee Endpoint Security
    TimeFormat = "dd/MM/yyyy HH:mm:ss a"
    Conditions = [ """<Custom McAfee USB Conditions>""" ]
    Fields = [
      """"EPO[^"]+"\|(".*?"\||[^|]*\|)\s*"({time}\d+\/\d+\/\d+ \d+:\d+:\d+ (am|AM|pm|PM))""",
      """"EPO[^"]+"\|(".*?"\||[^|]*\|){2}\s*"({host}[^"]+)""",
      """"EPO[^"]+"\|(".*?"\||[^|]*\|){3}\s*"(({domain}[^\\/"]+)[\\\/])?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
      """"EPO[^"]+"\|(".*?"\||[^|]*\|){5}\s*"({device_type}[^"]+)"""",
      """"EPO[^"]+"\|(".*?"\||[^|]*\|){6}\s*"({device_type}[^"]+)"""",
      """"EPO[^"]+"\|(".*?"\||[^|]*\|){5}\s*"({operation_details}[^"]+)""""
    ]
    ParserVersion = "v1.0.0"
  

}
```