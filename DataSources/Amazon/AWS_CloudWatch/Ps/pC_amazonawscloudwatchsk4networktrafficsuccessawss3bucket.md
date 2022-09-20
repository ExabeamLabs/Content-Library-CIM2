#### Parser Content
```Java
{
Name = amazon-awscloudwatch-sk4-network-traffic-success-awss3bucket
Vendor = "Amazon"
Product = "AWS CloudWatch"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """ requestClientApplication=AWS S3 Bucket"""
  """eni-"""
  """ OK """
]
Fields = [
  """cs6=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
  """\Wcs6=(\S+\s+){4}({src_ip}[a-fA-F\d.:]+)\s+({dest_ip}[a-fA-F\d.:]+)\s+({src_port}\d+)\s+({dest_port}\d+)(\s+\S+){2}\s+({bytes}\d+)"""
  """({result}\w+) OK\s*$"""
  """requestClientApplication=({app}[^=]+?)\s\w+="""
]
ParserVersion = "v1.0.0"


}
```