#### Parser Content
```Java
{
Name = amazon-ards-json-app-notification-success-configurationitemstatus
 Vendor = Amazon
 Product = Amazon RDS
 TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
 ParserVersion = v1.0.0
 Conditions = [""""configurationItemStatus":""",  """"configurationStateId":""", """"configurationItemCaptureTime":""" ]
 Fields = [
   """"configurationItemCaptureTime":({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)"""
   """"configurationItems":\[\{"configurationItemStatus":"({operation}[^"]+)"""
   """"awsAccountId":"({account_id}[^"]+)"""
   """"relationships":\[\{.+?"resourceType":"({resource_type}[^"]+)"""
   """"ARN":"({policy_arn}[^"]+)"""
 ]


}
```