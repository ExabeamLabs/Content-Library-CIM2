#### Parser Content
```Java
{
Name = nextdlp-r-json-policy-modify-success-reveal
  Vendor = NextDLP
  Product = Reveal
  ParserVersion = "v1.0.0"
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss","yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ" ,"yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSZ"]
  Conditions = [ """reveal""",""""policy_asset_changes":""",""""type":"PolicyAssetUpdated"""" ]
  Fields = [
    """"timestamp"+:\s*"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """"timestamp"+:\s*"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d{1,9}Z)"""
    """"type":"({event_name}[^",]+)""""
    """"policy_asset_name":"({policy_name}[^",]+)""""
    """"summary":"({description}[^,]+)""""
    """"type_id":({activity_id}\d+)"""
  ]


}
```