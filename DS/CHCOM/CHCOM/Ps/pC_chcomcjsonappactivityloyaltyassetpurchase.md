#### Parser Content
```Java
{
Name = chcom-c-json-app-activity-loyaltyassetpurchase
  Vendor = CHCOM
  Product = CHCOM
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = ["""chcom_loyaltyAssetPurchase""","""username""","""log_id""" ]
  Fields = [
    """@timestamp":"({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+Z)"""",
    """"host":\{"name":"({host}[^"]+)"""",
    """"username":"({user}[^"]+)"""",
    """"client_ip":"({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""",
    """"type":"({app}[^"]+)"""",
    """"source":"({object}[^"]+)"""",
    """"request_success":"({result}[^"]+)""""
    """"log_id":"({event_id}[^"]+)""""
  ]


}
```