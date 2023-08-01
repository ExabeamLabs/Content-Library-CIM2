#### Parser Content
```Java
{
Name = amazon-ards-json-app-notification-success-configurationitemchangenotification
 Vendor = Amazon
 Product = Amazon RDS
 TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
 ParserVersion = v1.0.0
 Conditions = [""""messageType":"ConfigurationItemChangeNotification"""", """"configurationItemDiff":""",  """"Relationships.""", """"changeType":""", """"notificationCreationTime":""" ]
 Fields = [
   """"notificationCreationTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)"""
   """""messageType"":"({event_name}[^"]+)"""
   """configurationItemDiff":\{"changedProperties":\{"Relationships\.\d+":\{"changeType":"({operation}[^"]+)"""
   """configurationItem":\{.+?"awsAccountId":"({account_id}[^"]+)"""
   """"relationships":\[\{.+?"resourceType":"({resource_type}[^"]+)"""
   """"ARN":"({policy_arn}[^"]+)"""
   """":\{"changedProperties":.+?previousValue":({old_value}[^\}]+})"""
 ]


}
```