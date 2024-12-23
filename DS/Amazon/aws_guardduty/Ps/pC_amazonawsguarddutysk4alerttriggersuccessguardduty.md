#### Parser Content
```Java
{
Name = amazon-awsguardduty-sk4-alert-trigger-success-guardduty
  Vendor = Amazon
  Product = AWS GuardDuty
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """Type: Discovery:S3/TorIPCaller""" ]
  Fields = [
    """CreatedAt:\s*({time}\d{4}-\d{2}-\d{2}T(\d{2}:){2}\d{2}\.\d+?Z),""",
    """IpAddressV4:\s*({src_ip}(\d{1,3}\.){3}\d{1,3}),""",
    """Title:\s*({event_name}[^:]+?),\w+?:""",
    """,Type:\s*({alert_type}[^:]+?):({alert_name}[^:]+?),\w+?:""",
    """Severity:\s*({alert_severity}[\d.]+),""",
    """Region:\s*({region}[^:]+?),\w+?:""",
    """Description:\s*({additional_info}[^:]+?),\w+?:""",
    """AccountId:\s*({account_id}[^:]+?),\w+?:"""
    """Resource:[^}]+PrincipalId:\s*([^},]+?(:({aws_email_address}({email_address}[^@]+@[^},]+)))?),UserName:\s*({aws_account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)),UserType:\s*({user_type}[^},]+)""",
    """ResourceType:\s*({resource_type}[^},]+)""",
    """S3BucketDetails:\s*\[\{Arn:\s*({object}[^,]+),Name:""",
  ]
  ParserVersion = "v1.0.0"


}
```