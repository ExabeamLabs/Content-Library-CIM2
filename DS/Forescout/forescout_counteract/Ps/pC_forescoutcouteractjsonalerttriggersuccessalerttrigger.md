#### Parser Content
```Java
{
Name = forescout-couteract-json-alert-trigger-success-alerttrigger
  ParserVersion = v1.0.0
  Vendor = Forescout
  Product = Forescout CounterACT
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """, "alertId":"""",""", "sensorName":"""",""", "engineName":"""",""", "feaAlertCount":"""",""", "feaAlertDetailCount":"""" ]
  Fields = [
    """exa_json_path=$.time,exa_field_name=time"""
    """exa_json_path=$.dstPort,exa_field_name=dest_port"""
    """exa_json_path=$.srcPort,exa_field_name=src_port"""
    """exa_regex="sensorName":"({host}[\w\-.]+)"""",
    """exa_regex="dstIp":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """exa_regex="srcHostName":"({src_host}[\w\-.]+)"""",
    """exa_regex="srcIp":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """exa_json_path=$.name,exa_field_name=alert_name"""
    """exa_json_path=$.typeId,exa_field_name=alert_type"""
    """exa_json_path=$.severity,exa_field_name=alert_severity"""
    """exa_json_path=$.desc,exa_field_name=additional_info"""
  ]


}
```