#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-notification-kernel
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = ["MMM dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ssZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ" ]
  Conditions = [ """ kernel: """ ]
  Fields = [
    """\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+))?""",
    """({time}\d\d\d\d-\d+-\d+T\d\d:\d\d:\d\d\.\d+[-+]\d\d:\d\d)\s+({host}[\w.\-]+)""",
    """({time}\w+\s*\d+ \d\d:\d\d:\d\d)\s*({host}[^\s]+)\s*kernel:""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d:\d\d)\s*({host}[^\s]+)\s*kernel""",
    """kernel:\s*({additional_info}.+?)\s*$""",
    """pid=({process_id}[^\s]+)\s\w+""",
    """comm="({process_name}[^\\"]+)"""",
    """operation="({operation}[^\s]+)""""
  ]


}
```