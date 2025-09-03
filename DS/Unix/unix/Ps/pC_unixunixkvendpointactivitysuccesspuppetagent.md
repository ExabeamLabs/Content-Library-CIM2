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
    """\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\[({service_id}\d+)\]\[({tag}\w+)\]""",
    """<\d+>\d+ ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)(\.\d+)?(\+|\-)\d\d:\d\d ({host}[\w.\-]+) ({service_name}puppet-agent) ({process_id}\d+) ({additional_info}.+?)\s*$""",
  ]


}
```