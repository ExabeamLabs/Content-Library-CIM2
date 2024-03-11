#### Parser Content
```Java
{
Name = forescout-couteract-json-alert-trigger-success-alerttrigger
  ParserVersion = v1.0.0
  Vendor = Forescout
  Product = Forescout CounterACT
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """, "alertId":"""",""", "sensorName":"""",""", "engineName":"""",""", "feaAlertCount":"""",""", "feaAlertDetailCount":"""" ]
  Fields = [
    """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d[+-]\d\d:\d\d)"""",
    """"sensorName":"({host}[\w\-.]+)"""",
    """"dstIp":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """"dstPort":"({dest_port}\d+)"""",
    """"srcHostName":"({src_host}[\w\-.]+)"""",
    """"srcIp":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"srcPort":"({src_port}\d+)"""",
    """"name":"({alert_name}[^"]+)"""",
    """"typeId":"({alert_type}[^"]+)"""",
    """"severity":"({alert_severity}[^"]+)"""",
    """"desc":"({additional_info}[^"]+)""""
  ]


}
```