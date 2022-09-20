#### Parser Content
```Java
{
Name = xiting-x-cef-app-activity-success-xams
  Vendor = Xiting
  Product = XAMS
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """CEF:""", """|Xiting|XAMS|""", """"SID":""""]
  Fields = [
    """"USERID":"({user}[^"]+)"""",
    """({app}XAMS)""",
    """"MSG":"({additional_info}[^"]+)"""",
    """"INSTANCE":"({target}[^"]+)"""",
    """"TASK_NAME":"({task_name}[^"]+)"""",
    """"TASK_NUMBER":"({task_number}[^"]+)"""",
    """"PROGRAME_NAME":"({programe_name}[^"]+)"""",
    """"TERMINAL":"({terminal}[^"]+)"""",
    """"TEXT":"({additional_info_2}[^"]+)"""",
    """"LOG_TIMESTAMP":({log_timestamp}\d+)"""
  ]
  ParserVersion = "v1.0.0"


}
```