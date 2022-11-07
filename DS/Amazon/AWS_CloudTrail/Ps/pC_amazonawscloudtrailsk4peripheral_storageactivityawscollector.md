#### Parser Content
```Java
{
Name = amazon-awscloudtrail-sk4-peripheral_storage-activity-awscollector
  ParserVersion = v1.0.0
  Vendor = Amazon
  Product = AWS CloudTrail
  TimeFormat = "dd/MMM/yyyy:HH:mm:ss"
  Conditions = ["""requestClientApplication=AWS Collector""", """ arn:aws""" , """.amazonaws.com """ ]
  Fields = [
    """\s({bucket_name}\S+)\s\[\d\d\/\w\w\w\/\d\d\d\d:\d\d:\d\d:\d\d""",
    """\[({time}\d\d\/\w\w\w\/\d\d\d\d:\d\d:\d\d:\d\d)""",
    """\d\d\d\d:\d\d:\d\d:\d\d\s\+\d\d\d\d\]\s({src_ip}[^\s]+)""",
    """:assumed-role\/({access}[^\/]+\/({user}[^\/\s]+))""",
    """assumed-role\/({user}[^\/]+)"""
    """\s(REST|BATCH)\.({method}\w+)""",
    """\s(REST|BATCH)\.\w+\.\w+\s(({file_path}({file_dir}[^\s]*)\/({file_name}[^\s\/]+)))\s""",
    """\s(REST|BATCH)\.\w+\.\w+\s\S+\s"[^"]+"\s({result}\d+)""",
    """\s(REST|BATCH)\.\w+\.\w+\s(-|[^\s]+)\s"[^"]+"\s({result}[^\s]+)\s(-|({failure_reason}[^\s]+))\s(-|({bytes_out}\d+))\s(-|[^\s]+)\s(-|[^\s]+)\s(-|[^\s]+)\s"(-|[^\s]+)"\s"(-|({user_agent}[^"]+))"\s"""
    """({service_name}s3.amazonaws.com)""",
    """\s({operation}(REST|BATCH)\.\w+\.\w+)""",
  ]
  DupFields = [ "access->role", "file_path->object" ]


}
```