#### Parser Content
```Java
{
Name = venofi-tlp-json-app-activity-success-tls
    Vendor = Venafi
    Product = TLS Protect
    TimeFormat = "yyyy-MM-dd HH:mm:ssZ"
    ParserVersion = "v1.0.0"
    Conditions = [ """"grouping":""", """"description":"""", """event_id"""", """"time_stamp"""" ]
    Fields = [
      """"time_stamp":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\dZ)"""
      """({host}[\w\-\.]+)\s*\{"data""""
      """"description":"({additional_info}[^"]+)"""
      """"text1":\{"name".+?"value":"[^:]+:({user}[\w\-\.]+)"\}"""
      """"event_id":"({event_code}[^"]+)""""
      """""grouping":\{.+?"object":"({object}[^"]+)"""
      """"severity":({severity}\d)"""
      """"object_id":({object_id}\d+)"""
      """"dvc_ip":"({device_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""""
    ]
    DupFields = ["additional_info->event_name"]


}
```