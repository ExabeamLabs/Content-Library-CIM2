#### Parser Content
```Java
{
Name = amazon-awscloudwatch-sk4-network-traffic-success-awsflowlogs
Vendor = "Amazon"
Product = "AWS CloudWatch"
TimeFormat = "epoch_sec"
Conditions = [
  """ eni-"""
  """requestClientApplication=AWS-FlowLogs"""
]
Fields = [
  """cs6=\d+\s+(unknown|({account_id}\S+))\s+({interface_id}\S+)\s+(-|({src_ip}[A-Fa-f:\d.]+))\s+(-|({dest_ip}[A-Fa-f:\d.]+))\s+(-|({src_port}\d+))\s+(-|({dest_port}\d+))\s+(-|({protocol}\S+))\s+(-|({packets}\d+))\s+(-|({bytes}\d+))\s+({time}\d+)\s+\S+\s+(-|({action}\S+))\s+(-|({result}\S+))"""
]
ParserVersion = "v1.0.0"


}
```