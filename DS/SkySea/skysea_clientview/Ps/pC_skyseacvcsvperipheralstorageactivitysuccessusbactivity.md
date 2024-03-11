#### Parser Content
```Java
{
Name = skysea-cv-csv-peripheral-storage-activity-success-usbactivity
  Vendor = SkySea
  Product = SkySea ClientView
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [ """,ドライブ,""", """,ドライブの追加,""" ]
  Fields = [
    """({host}[^,]+),([^,]*,){7}ドライブ,""",
    """({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+)),([^,]*,){6}ドライブ,""",
    """({user}[^,]+),([^,]*,){4}ドライブ,""",
    """({time}\d{4}\/\d\d\/\d\d \d\d:\d\d:\d\d),ドライブ,""",
    """,ドライブ,([^,]*,){2}({target}[^,]+),""",
    """,ドライブ,([^,]*,){15}(-|({device_id}[^,]+)),""",
    """,ドライブ,([^,]*,){12}({device_name}[^,]+),""",
    """,({operation}ドライブの追加),""",
    """,ドライブ,([^,]*,){29}({device_type}[^,]+),""",
    """({host}[\w\-.]+),\d+,""",
    """^([^\,]*\,){3}({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\,""",
    """^([^\,]*\,){5}({user}[^\,]+)\,""",
    """^([^\,]*\,){7}({time}\d+\/\d+\/\d+ \d+:\d+:\d+)""",
  ]
  ParserVersion = "v1.0.0"


}
```