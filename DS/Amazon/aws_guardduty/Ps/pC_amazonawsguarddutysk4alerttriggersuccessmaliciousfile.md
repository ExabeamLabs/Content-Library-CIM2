#### Parser Content
```Java
{
Name = amazon-awsguardduty-sk4-alert-trigger-success-maliciousfile
  Conditions = [ """,ServiceName: guardduty,""", """,Type: Execution:Kubernetes/MaliciousFile,""" ]
  ParserVersion = "v1.0.0"

cef-aws-guardduty-security-alert-template-1 = {
    Vendor = Amazon
    Product = AWS GuardDuty
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """,CreatedAt:\s*({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ),""",
      """,LocalIpDetails:[^\}]+IpAddressV4:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """,RemoteIpDetails:[^\]]+IpAddressV4:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """,Title:\s*({event_name}[^:]+?)\.?,\w+:""",
      """,Type:\s*({alert_type}[^:]+):({alert_name}[^:]+?),\w+:""",
      """,Severity:\s*({alert_severity}[^,]+),""",
      """,Region:\s*({region}[^:]+),\w+:""",
      """,Description:\s*({additional_info}[^:]+?)\.?,\w+:""",
      """AccountId:\s*({account_id}[^,]+),""",
      """ResourceType:\s*({resource_type}[^,\}]+)""",
      """,Arn:\s*({object}[^,]+),\w+:""",
      """,UserName:\s*({aws_account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
      """,UserType:\s*({user_type}[^,\}]+)"""
    
}
```