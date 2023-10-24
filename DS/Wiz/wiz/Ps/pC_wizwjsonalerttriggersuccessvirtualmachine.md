#### Parser Content
```Java
{
Name = wiz-w-json-alert-trigger-success-virtualmachine
  Vendor = Wiz
  Product = Wiz
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """"type":"Created"""", """"severity":"""", """"name":"""", """"trigger":{"""", """"cloudPlatform":"""" ]
  Fields = [
    """"created":"({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)"""",
    """"control":\{[^\}]+?"id":"({alert_id}[^"]+)"""",
    """"control":\{[^\}]+?"name":"({alert_name}[^"]+)"""",
    """"resource":\{[^\}]+?"type":"({alert_type}[^"]+)"""",
    """"control":\{"severity":"({alert_severity}[^"]+)"""",
    """({app}wiz)""",
    """"ruleName":"({rule}[^"]+)"""",
    """"ruleId":"({rule_id}[^"]+)"""",
    """"region":"({region}[^"]+)"""",
    """"trigger":\{[^\}]+?"type":"({operation}[^"]+)"""",
    """"description":"({additional_info}[^"]+)""""
  ]


}
```