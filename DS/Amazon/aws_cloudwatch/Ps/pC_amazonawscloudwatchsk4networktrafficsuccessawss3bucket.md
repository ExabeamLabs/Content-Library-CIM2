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
    """\Wcs6=(\S+\s+){4}({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s+({src_port}\d+)\s+({dest_port}\d+)(\s+\S+){2}\s+({bytes}\d+)"""
    """({result}\w+) OK\s*$"""
    """requestClientApplication=({app}[^=]+?)\s\w+="""
  ]
  ParserVersion = "v1.0.0"


}
```