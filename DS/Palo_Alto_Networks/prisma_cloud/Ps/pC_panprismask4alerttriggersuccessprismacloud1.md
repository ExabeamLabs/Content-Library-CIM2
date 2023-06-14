#### Parser Content
```Java
{
Name = pan-prisma-sk4-alert-trigger-success-prismacloud-1
  ParserVersion = v1.0.0
  Vendor = Palo Alto Networks
  Product = Prisma Cloud
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [  """destinationServiceName =""", """"service":"Prisma Cloud"""", """"policy":""", """"policyType":""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)\s[\w\-.]+\s+""",
    """"name":"({alert_name}[^"]+)","policyTs":"""",
    """"policy":\{[^\}]+,"name":"({alert_name}[^"]+)"""",
    """"severity":"({alert_severity}[^"]+)"""",
    """"alertId":"({alert_id}[^"]+)"""",
    """"description":"({additional_info}[^"]+)"""",
    """"service":"({app}[^"]+)"""",
    """"account":\{[^}]+,"name":"({user}[^"]+)"""",
    """"alertRuleName":"({alert_type}[^"]+)"""",
    """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
    ]


}
```