#### Parser Content
```Java
{
Name = "amazon-awsvpc-sk4-network-traffic-success-transitgateway"
  ParserVersion = "v1.0.0"
  Vendor = "Amazon"
  Product = "VPC Flow Logs"
  TimeFormat = "epoch_sec"
  Conditions = [
    """ eni-"""
    """ TransitGateway """
    """ tgw-attach-"""
    """ vpc-"""
  ]
  Fields = [
    """requestClientApplication=({host}[^\s]+)\s"""
    """({resource_type}TransitGateway)\s({account_id}\S+)\s([^\s]+\s){2}({user_id}\S+)\s({dest_user_id}\S+)\s({vpc}\S+)\s([^\s]+)\s([^\s]+\s){4}({src_network_zone}\S+)\s({dest_network_zone}\S+)\s[^\s]+\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s+({src_port}\d+)\s+({dest_port}\d+)\s+({protocol}\w+)\s+({packets}\d+)\s+({bytes}\d+)\s+({time}\d{10})(\d+)? \S+ ({action}\S+)\s(\w+)\s+([^\s]+\s){5}({region}[^\s]+)\s({direction}egress|ingress)"""
  ]


}
```