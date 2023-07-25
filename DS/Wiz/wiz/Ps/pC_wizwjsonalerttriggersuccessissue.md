#### Parser Content
```Java
{
Name = wiz-w-json-alert-trigger-success-issue
  Vendor = Wiz
  Product = Wiz
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """"source":"ISSUE"""", """"updatedFields":"""", """"status":"""", """"subscriptionName":"""", """"changedBy":"Wiz"""" ]
  Fields = [
    """"created":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,6}Z)"""",
    """"severity":"({severity}[^"]+)"""",
    """"control":\{[^\}]+?"name":"({event_name}[^"]+?)\s*"""",
    """"updatedFields":"\s*({additional_info}[^"]+?)\s*"""",
    """"ruleName":"({rule}[^"]+)"""",
    """"ruleId":"({rule_id}[^"]+)""""
    """"subscriptionId":"({subscription_id}[^"]+)""""
  ]
  ParserVersion = v1.0.0


}
```