#### Parser Content
```Java
{
Name = xiting-x-cef-app-activity-success-xams
  Vendor = Xiting
  Product = XAMS
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """CEF:""", """|Xiting|XAMS|""", """"SID":""""]
  Fields = [
    """"USERID":"({user}[\w\.\-]{1,40}\$?)"""",
    """({app}XAMS)""",
    """"MSG":"({additional_info}[^"]+)"""",
    """"INSTANCE":"({target}[^"]+)"""",
    """"TASK_NAME":"({task_name}[^"]+)"""",
# task_number is removed
# programe_name is removed
    """"TERMINAL":"({terminal}[^"]+)"""",
    """"TEXT":"({additional_info_2}[^"]+)"""",
# log_timestamp is removed
  ]
  ParserVersion = "v1.0.0"


}
```