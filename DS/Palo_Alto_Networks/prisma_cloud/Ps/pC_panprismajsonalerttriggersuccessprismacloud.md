#### Parser Content
```Java
{
Name = pan-prisma-json-alert-trigger-success-prismacloud
  Vendor = Palo Alto Networks
  Product = Prisma Cloud
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [""""alertRuleName":""", """"app":"Prisma Cloud Alert Notification"""", """"source":"Prisma Cloud"""", """"policyName":"""]
  Fields = [ 
    """"policyName":"({alert_name}[^"]+)"""",
    """"severity":"({alert_severity}[^"]+)"""",
    """"alertId":"({alert_id}[^"]+)"""",
    """"callbackUrl":"({additional_info}[^"]+)"""",
    """"source":"({app}[^"]+)"""",
    """"url":"({url}[^"]+)"""",
    """"policyId":"({policy_id}[^"]+)"""",
    """"accountName":"({user}[^"]+)"""",
    """"alertRuleName":"({alert_type}[^"]+)"""
  ]


}
```