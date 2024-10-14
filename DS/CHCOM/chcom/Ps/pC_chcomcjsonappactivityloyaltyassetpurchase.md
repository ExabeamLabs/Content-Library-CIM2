#### Parser Content
```Java
{
Name = chcom-c-json-app-activity-loyaltyassetpurchase
  Vendor = CHCOM
  Product = CHCOM
  ExtractionType = json
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = ["""chcom_loyaltyAssetPurchase""","""username""","""log_id""" ]
  Fields = [
    """exa_json_path=$.@timestamp,exa_field_name=time""",
    """exa_json_path=$.host.name,exa_field_name=host""",
    """exa_json_path=$.username,exa_regex=({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """exa_json_path=$.client_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.type,exa_field_name=app""",
    """exa_json_path=$.source,exa_field_name=object""",
    """exa_json_path=$.request_success,exa_field_name=result"""
    """exa_json_path=$.log_id,exa_field_name=event_id"""
  ]


}
```