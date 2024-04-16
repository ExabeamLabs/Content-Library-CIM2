#### Parser Content
```Java
{
Name = microsoft-azuresc-json-alert-trigger-success-security
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Azure Monitor
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions = [ """"correlationId":"""", """"localizedValue":"""", """"Microsoft.Security"""", """"eventName":{"value":""" ]
  Fields = [
    """"eventTimestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""",
    """"description":"({additional_info}[^"]+)"""",
    """"Severity":"({alert_severity}[^"]+)"""",
    """"eventName":\{"value":"({alert_name}[^"]+)"""",
    """"category":\{"value":"({alert_type}[^"]+)"""",
    """"UserSID":"({user_sid}[^"]+)"""",
    """"processName":"({process_name}[^"]+)"""",
    """"userName":"({user}[^"]+)""""
 ]


}
```