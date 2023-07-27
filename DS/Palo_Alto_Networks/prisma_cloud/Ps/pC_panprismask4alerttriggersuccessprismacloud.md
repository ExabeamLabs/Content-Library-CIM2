#### Parser Content
```Java
{
Name = pan-prisma-sk4-alert-trigger-success-prismacloud
  ParserVersion = v1.0.0
  Vendor = Palo Alto Networks
  Product = Prisma Cloud
  TimeFormat = """yyyy-MM-dd'T'HH:mm:ss.SSSZ"""
  Conditions = [""""alertRuleName":""", """destinationServiceName =""", """"source":"Prisma Cloud"""", """"policyName":"""]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)\s[\w\-.]+\s+""",
    """"privateIpAddresses":\[.+?"privateIpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"policyName":"({alert_name}[^"]+)"""",
    """"severity":"({alert_severity}[^"]+)"""",
    """"alertId":"({alert_id}[^"]+)"""",
    """"callbackUrl":"({additional_info}[^"]+)"""",
    """"source":"({app}[^"]+)"""",
    """"url":"({url}[^"]+)"""",
    """"policyId":"({policy_id}[^"]+)"""",
    """"accountName":"({user}[\w\.\-]{1,40}\$?)"""",
    """"alertRuleName":"({alert_type}[^"]+)"""
  ]


}
```