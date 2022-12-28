#### Parser Content
```Java
{
Name = unix-unix-kv-endpoint-activity-success-puppetagent
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """][""", """ puppet-agent """ ]
  Fields = [
    """\[({src_ip}[a-fA-F\d.:]+)\]\[({service_id}\d+)\]\[({tag}\w+)\]""",
    """<\d+>\d+ ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)(\.\d+)?(\+|\-)\d\d:\d\d ({host}[\w.\-]+) ({service_name}puppet-agent) ({process_id}\d+) ({additional_info}.+?)\s*$""",
  ]


}
```