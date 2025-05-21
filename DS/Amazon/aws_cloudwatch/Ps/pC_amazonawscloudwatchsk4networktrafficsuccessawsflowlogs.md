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
    """cs6=\d+\s+(unknown|({account_id}\S+))\s+({interface_id}\S+)\s+(-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s+(-|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)\s+(-|({=src_port}\d+))\s+(-|({=dest_port}\d+))\s+(-|({protocol}\S+))\s+(-|({packets}\d+))\s+(-|({bytes}\d+))\s+({time}\d{10})\s+\S+\s+(-|({action}\S+))\s+(-|({result}\S+))"""
  ]
  ParserVersion = "v1.0.0"


}
```