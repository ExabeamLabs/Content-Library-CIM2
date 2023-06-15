#### Parser Content
```Java
{
Name = amazon-awsguardduty-sk4-alert-trigger-success-guardduty-3
  Vendor = Amazon
  Product = AWS GuardDuty
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"source":"aws.guardduty"""", """"detail-type":"GuardDuty Finding"""" ]
  Fields = [
    """"createdAt":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """suser=(?:(?i)anonymous|({user}[^=]+?))\s+\w+=""",
    """"severity":({alert_severity}\d+)""",
    """"title":"({alert_name}[^"]+)""",
    """"description":"({additional_info}[^"]+)""",
    """"type":"({alert_type}[^"]+)""",
    """"resource":[^=]+?privateIpAddress":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"remoteIpDetails[^=]+?"ipAddressV4":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"remotePortDetails":\{"port":({src_port}\d+)""",
    """"localPortDetails":\{"port":({dest_port}\d+)""",
    """requestClientApplication=({app}[^=]+?)\s+\w+=""",
    """"accountId":"({account_id}\d+)""",
    """"country":\{"countryName":"({country_name}[^"]+)""",
    """"city":\{"cityName":"((?i)UNKNOWN|({location_city}[^"]+))""",
    """UnauthorizedAccess:EC2\/SSHBruteForce[^\}\]]*"instanceId":"({instance_id}[^"]+)""",
    """UnauthorizedAccess:EC2\/SSHBruteForce[^=]+?"availabilityZone":"({availability_zone}[^"]+)""",
    """"principalId":"({principal_id}[^"]+)""",
    """Recon:IAMUser\/UserPermissions[^\}\]]*"principalId":"({principal_id}[^"]+)""",
    """"userName":"(({email_address}[^@"]+@[^"]+)|({user}[^"]+))""",
    """"s3BucketDetails":[^\}\]]*"name":"({s3_bucket_name}[^"]+)""",
    """securityGroups":[^"]+"groupName":"({group_name}[^"]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```