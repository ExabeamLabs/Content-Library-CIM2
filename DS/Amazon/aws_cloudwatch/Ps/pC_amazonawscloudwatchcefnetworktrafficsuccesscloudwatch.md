#### Parser Content
```Java
{
Name = "amazon-awscloudwatch-cef-network-traffic-success-cloudwatch"
  ParserVersion = "v1.0.0"
  Vendor = "Amazon"
  Product = "AWS CloudWatch"
  TimeFormat = "epoch"
  Conditions = [
    """destinationServiceName =AWS"""
    """dproc=CloudWatch Logs"""
  ]
  Fields = [
    """\Wstart=({time}\d{13})"""
    """\Wend=({time}\d{13})"""
    """\Wcat=(|({category}[^=]+?))(\s+\w+=|\s*$)"""
    """\Wcn2=({bytes}\d+)"""
    """\WdestinationServiceName =(|({service_name}[^=]+?))(\s+\w+=|\s*$)"""
    """\Wdpt=({dest_port}\d+)"""
    """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """\Wspt=({src_port}\d+)"""
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """\Wproto=(|({protocol}[^=]+?))(\s+\w+=|\s*$)"""
    """\Wsuser=(|anonymous|({aws_account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))(\s+\w+=|\s*$)"""
    """\Wact=(|({action}[^=]+?))(\s+\w+=|\s*$)"""
  ]


}
```