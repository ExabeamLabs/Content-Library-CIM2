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
    """"client_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"type":"({app}[^"]+)"""",
    """"source":"({object}[^"]+)"""",
    """"request_success":"({result}[^"]+)""""
    """"log_id":"({event_id}[^"]+)""""
  ]


}
```