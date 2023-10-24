#### Parser Content
```Java
{
Name = amazon-awsguardduty-json-database-login-success-rdssuccessfullogin
  Conditions = [ """"serviceName":"guardduty"""", """"type":"CredentialAccess:RDS/AnomalousBehavior.SuccessfulLogin"""" ]
  ParserVersion = "v1.0.0"

cef-aws-guardduty-security-alert-template = {
    Vendor = Amazon
    Product = AWS GuardDuty
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """"updatedAt":\s*"({time}\d{4}-\d{2}-\d{2}T(\d{2}:){2}\d{2}\.\d+Z)",""",
      """"ipAddressV4":\s*"({src_ip}(\d{1,3}\.){3}\d{1,3})"""",
      """"title":"(({event_name}[^"]+?(instance|bucket|database))(\s[^"\s]+?)?|({=event_name}[^"]+?))",""",
      """"type":"({alert_type}[^"]+):({alert_name}[^"]+)",""",
      """"severity":\s*({alert_severity}[\d.]+),""",
      """"region":\s*"({region}[^"]+?)",""",
      """"description":\s*"({additional_info}[^"]+?)"""",
      """"accountId":\s*"({account_id}[^"]+?)","""
      """domain":"({domain}[^"]+)"""",
      """resource":[^}]+principalId":\s*"([^},]+?(:({email_address}[^@]+@({email_domain}[^},]+)))?)"""",
      """resource":[^}]+"userName":\s*"({user}[\w\.-]{1,99}\$?)"""",
      """resource":[^}]+"userType":\s*"({user_type}[^},]+?)"""",
      """key":"PrincipalId","value":"([^:]+:)?({email_address}[^@]+@({email_domain}[^},"]+?))"""",
      """"resourceType":\s*"({resource_type}[^"]+)"""",
      """S3BucketDetails:\s*\[\{Arn:\s*({object}[^,]+),Name:""",
    
}
```