#### Parser Content
```Java
{
Name = "zeek-zeek-json-app-notification-software"
  Vendor = "Zeek"
  Product = "Zeek"
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """"_path":"software""",""""software_type":"""", """"_system_name":"""", """"host":""""]
  Fields = [
    """"ts":"({time}\d\d\d\d-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}\.\d+Z)"""",
    """"_system_name":"({host}[\w\-.]+)"""",
    """"host":"({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""",
    """"name":"({app}[^"]+)"""",
# software_type is removed
  ]


}
```