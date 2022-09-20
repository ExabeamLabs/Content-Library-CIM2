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
    """"aip":"({src_ip}[a-fA-F\d:\.]+)"""",
    """"name":"({event_name}[^"]+)"""",
    """"event_simpleName":"({event_code}[^"]+)"""",
    """"TargetFileName":"({src_file_path}(({file_dir}[^"]*?)[\\\/]+)?\s*({src_file_name}[^\\\/"]+?(\.(\d+|({src_file_ext}[^\\\/"\.]+)))?))"""",
    """"Size":"({bytes}\d+)"""",
    """"DiskParentDeviceInstanceId":"({device_id}[^"]{1,2099})"""",
    """"aid":"({aid}[^"]+)""""  
  ]
  DupFields = [ "device_id->service_type" ]
  ParserVersion = v1.0.0


}
```