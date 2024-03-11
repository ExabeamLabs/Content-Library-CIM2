#### Parser Content
```Java
{
Name = ironnet-id-json-alert-trigger-success-irondefense
  ParserVersion = v1.0.0
  Vendor = IronNet
  Product = IronDefense
  TimeFormat =  "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"app":"irondefense"""", """"type":"event"""", """"alert_status":"""", """"severity":"""", """"alert_aggregation_criteria":""""  ]
  Fields = [
    """"start_time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""",
    """"subject":"({alert_name}[^",]+)"""",
    """"src_category":"({alert_type}[^",]+)"""",
    """"severity":"({alert_severity}[^"]+)"""",
    """"alert_status":"({alert_status}[^",]+)"""",
    """"src_ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"dst_ip":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """"dst_port":({dest_port}\d+)""",
    """"bytes_out":({bytes_out}\d+)""",
    """"body":"({additional_info}[^",]+)""""
  ]


}
```