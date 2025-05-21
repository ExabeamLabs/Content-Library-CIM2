#### Parser Content
```Java
{
Name = "amazon-awscloudwatch-mix-network-traffic-success-accept"
  ParserVersion = "v1.0.0"
  Vendor = "Amazon"
  Product = "AWS CloudWatch"
  TimeFormat = "epoch_sec"
  Conditions = [
    """ eni-"""
    """ ACCEPT OK"""
  ]
  Fields = [
    """requestClientApplication=({host}[^\s]+)\s"""
    """(unknown|({account_id}\S+)) ({interface_id}\S+) ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})) ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})) ({src_port}\d+) ({dest_port}\d+) ({protocol}\S+) ({packets}\d+) ({bytes}\d+) ({time}\d{10})(\d+)? \S+ ({action}\S+) ({result}[^\"\\\s]+)"""
  ]


}
```