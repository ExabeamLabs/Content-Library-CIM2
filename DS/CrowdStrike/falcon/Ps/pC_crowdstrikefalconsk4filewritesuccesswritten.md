#### Parser Content
```Java
{
Name = crowdstrike-falcon-sk4-file-write-success-written
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """ destinationServiceName =CrowdStrike """, """"IsOnRemovableDisk":"1"""", """"event_simpleName":"""", """Written""" ]
  Fields = [
    """"timestamp":"({time}\d{13})"""",
    """"UserName":"({user}[^"]+)"""",
    """"aip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"name":"({event_name}[^"]+)"""",
    """"event_simpleName":"({event_code}[^"]+)"""",
    """"TargetFileName":"({file_path}(({file_dir}[^"]*?)[\\\/]+)?\s*({file_name}[^\\\/"]+?(\.(\d+|({file_ext}[^\\\/"\.]+)))?))"""",
    """"Size":"({bytes}\d+)"""",
    """"DiskParentDeviceInstanceId":"({device_id}[^"]{1,2099})"""",
    """"aid":"({aid}[^"]+)""""  
  ]
  DupFields = [ "device_id->service_type" ]
  ParserVersion = v1.0.0


}
```