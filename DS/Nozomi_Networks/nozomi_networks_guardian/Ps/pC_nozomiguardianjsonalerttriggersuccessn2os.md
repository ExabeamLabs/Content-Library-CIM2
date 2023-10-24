#### Parser Content
```Java
{
Name = nozomi-guardian-json-alert-trigger-success-n2os
    Vendor = Nozomi Networks
    Product = Nozomi Networks Guardian
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Conditions = [""""vendor_product":"Nozomi_Networks_N2OS"""", """"nozomi_source":"alerts"""", """"category":"""]
    Fields = [
      """"_time":"({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}(\+|-)\d{2}:\d{2})""",
      """"dvc_host":"({host}[\w.-])",""",
      """"nozomi_type_id":"({alert_type}[^"]+)"""",
      """"category":"({alert_name}[^"]+)"""",
      """"nozomi_id":"({alert_id}[^"]+)"""",
      """"severity":"({alert_severity}[^"]+)"""",
      """"description":"({additional_info}[^"]+)"""",
      """"src_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
      """"dest_ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
      """"src_mac":"({src_mac}[a-fA-F\d:]+)""",
      """"dest_mac":"({dest_mac}[a-fA-F\d:]+)""",
      """"src_port":({src_port}\d+)""",
      """"dest_port":({dest_port}\d+)""",
      """"dest_host":"({dest_host}[\w.-]+)""",
     ]


}
```