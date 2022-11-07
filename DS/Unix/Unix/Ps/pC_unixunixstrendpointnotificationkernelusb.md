#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-notification-kernelusb
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ kernel: usb """ ]
  Fields = [
    """\d\d:\d\d:\d\d\s({dest_ip}[^\s]+)\s*({host}[^\s]+)\s*kernel:""",
    """\skernel:\s*({additional_info}.+?)\s*$""",
  ]


}
```