#### Parser Content
```Java
{
Name = microsoft-azuresc-sk4-alert-trigger-success-logactivity
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Azure Monitor
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"correlationId":"""", """"localizedValue":"""", """"Microsoft.Security"""", """"containerImage":"""", """dproc=Activity Log""" ]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+Z)\s+[^\s]+\s+""",
    """msg=({additional_info}.+?)\s+(\w+=|$)""",
    """"operationName":\{"value":"({operation}[^"]+)"""",
    """request=({result}.+?)\s*\w+=""",
    """"severity":"({alert_severity}[^"]+)""",
    """"eventName":\{"value":"({alert_name}[^"]+)"""",
    """sourceServiceName =\s*({service_name}.+?)\s+\w+""",
    """suser=(Azure Security Center|({user}[\w\.\-]{1,40}\$?))\s+\w+=""",
    """intent":"\[\\"({alert_type}[^\\"]+)""",
 ]


}
```