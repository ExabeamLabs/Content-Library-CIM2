#### Parser Content
```Java
{
Name = skysea-cv-kv-alert-trigger-success-tcp
  Vendor = SkySea
  Product = SkySea ClientView
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [""",想定外TCP通信,""" ]
  Fields = [
    """^([^\,]*\,){2}({src_host}[^\,]+)\,""",
    """^([^\,]*\,){3}({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\,""",
    """^([^\,]*\,){5}(SYSTEM|({user}[\w\.\-]{1,40}\$?))\,""",
    """^([^\,]*\,){7}({time}\d+\/\d+\/\d+ \d+:\d+:\d+)""",
    """^([^\,]*\,){68}({process_path}({process_dir}(?:(\w+:)*([\\\/]+[^\\\/"]+)+)?[\\\/]+)({process_name}[^\,\\\/]+))\,""",
    """^([^\,]*\,){69}({hash_md5}[^\,]+)\,""",
    """^([^\,]*\,){70}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\,""",
    """^([^\,]*\,){71}({dest_port}\d+)\,""",
    """^([^\,]*\,){73}({bytes_out}\d+)\,""",
    """^([^\,]*\,){74}({bytes_in}\d+)\,""",
    """^([^\,]*\,){8}({alert_name}[^\,]+)\,""",
    """^([^\,]*\,){72}({additional_info}[^\,]+)\,""",
  ]


}
```