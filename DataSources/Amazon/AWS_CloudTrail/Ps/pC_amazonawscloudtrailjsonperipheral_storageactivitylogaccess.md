#### Parser Content
```Java
{
Name = amazon-awscloudtrail-json-peripheral_storage-activity-logaccess
  ParserVersion = v1.0.0
  Vendor = Amazon
  Product = AWS CloudTrail
  TimeFormat = "dd/MMM/yyyy:HH:mm:ss Z"
  Conditions = [ """"aws:s3:accesslogs"""", """sourcetype"""]
  Fields = [
    """({bucket_name}\S+)\s\[({time}\d\d\/\w\w\w\/\d\d\d\d:\d\d:\d\d:\d\d\s[+-]\d\d\d\d)\]\s(-|({src_ip}[A-Fa-f\d:.]+))\s\S+\s\S+\s(-|({operation}\S+))\s\S+\s\S+\s\S+\s\S+\s\S+\s(-|({failure_reason}\S+))\s\S+\s\S+\s\S+\s\S+\s\S+\s((\\\\)?"(-|({user_agent}[^"\\]+)))?""",
    """\[(\d\d\/\w{1,4}\/\d\d\d\d:\d\d:\d\d:\d\d\s[+-]\d\d\d\d)\](\s\S+){15}\s[\\"]*[^"]+"(\s\S+){5}\s({service_name}[\w\-.]+)""",
  ]
  DupFields = [ "service_name->host" ]


}
```