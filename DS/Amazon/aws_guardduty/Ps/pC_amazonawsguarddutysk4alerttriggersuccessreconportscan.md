#### Parser Content
```Java
{
Name = amazon-awsguardduty-sk4-alert-trigger-success-reconportscan
  Conditions = [ """CEF:""", """requestClientApplication=AWS_GUARDDUTY""", """"type":"Recon:EC2/Portscan"""" ]
  ParserVersion = "v1.0.0"

cef-aws-guardduty-security-alert-template = {
    Vendor = Amazon
    Product = AWS GuardDuty
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """"updatedAt":\s*"({time}\d{4}-\d{2}-\d{2}T(\d{2}:){2}\d{2}\.\d+Z)"""",
      """"ipAddressV4":\s*"({src_ip}(\d{1,3}\.){3}\d{1,3})"""",
      """"title":"(({event_name}[^"]+?(instance|bucket|database))(\s[^"\s]+?)?|({=event_name}[^"]+?))",""",
      """"type":"({alert_type}[^"]+):({alert_name}[^"]+)",""",
      """"severity":\s*({alert_severity}[\d.]+),""",
      """"region":\s*"({region}[^"]+?)",""",
      """"description":\s*"({additional_info}[^"]+?)"""",
      """"accountId":\s*"({account_id}[^"]+?)","""
      """domain":"({domain}[^"]+)"""",
      """resource":[^}]+principalId":\s*"([^},]+?(:({aws_email_address}({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))))?)"""",
      """resource":[^}]+"userName":\s*"({aws_account}({user}[\w\.-]{1,99}\$?))"""",
      """resource":[^}]+"userType":\s*"({user_type}[^},]+?)"""",
      """key":"PrincipalId","value":"([^:]+:)?({aws_email_address}({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))"""",
      """"resourceType":\s*"({resource_type}[^"]+)"""",
      """s3BucketDetails:\s*\[\{Arn:\s*({object}[^,]+),Name:""",
      """"resource":[^=]+?privateIpAddress":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """"service".*?"action".*?"portProbeAction".*?"portProbeDetails".*?"localPortDetails".*?"port":"({dest_port}\d+)"""",
      """"instanceId":"({instance_id}[^"]+)""",
      """"city":\{"cityName":"((?i)UNKNOWN|({location_city}[^"]+))"""
      """"key":"ProductOwner","value":"({aws_email_address}({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))""""
    
}
```