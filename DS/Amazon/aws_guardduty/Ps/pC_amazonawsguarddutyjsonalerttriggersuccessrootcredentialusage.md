#### Parser Content
```Java
{
Name = amazon-awsguardduty-json-alert-trigger-success-rootcredentialusage
  Conditions = [ """"serviceName":"guardduty"""", """"type":"Policy:IAMUser/RootCredentialUsage"""" ]
  ParserVersion = "v1.0.0"

cef-aws-guardduty-security-alert-template = {
    Vendor = Amazon
    Product = AWS GuardDuty
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """"createdAt":\s*"({time}\d{4}-\d{2}-\d{2}T(\d{2}:){2}\d{2}\.\d+Z)",""",
      """"ipAddressV4":\s*"({src_ip}(\d{1,3}\.){3}\d{1,3})"""",
      """"title":"({event_name}[^"]+)",""",
      """"type":"({alert_type}[^"]+):({alert_name}[^"]+)",""",
      """"severity":\s*({alert_severity}[\d.]+),""",
      """"region":\s*"({region}[^"]+?)",""",
      """"description":\s*"({additional_info}[^"]+?)",""",
      """"accountId":\s*"({account_id}[^"]+?)","""
      """domain":"({domain}[^"]+)"""",
      """resource":[^}]+principalId":\s*"([^},]+?(:({email_address}[^@]+@[^},]+))?)","userName":\s*"({user}[^},]+?)","userType":\s*"({user_type}[^},]+?)"""",
      """key":"PrincipalId","value":"([^:]+:)?({email_address}[^@]+@[^},"]+?)"""",
      """"resourceType":\s*"({resource_type}[^"]+)"""",
      """S3BucketDetails:\s*\[\{Arn:\s*({object}[^,]+),Name:""",
    
}
```