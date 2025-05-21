#### Parser Content
```Java
{
Name = crowdstrike-falcon-sk4-file-write-success-written
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = ["epoch", "epoch_sec"]
  Conditions = [ """CEF:""", """ destinationServiceName =CrowdStrike """, """"IsOnRemovableDisk":"1"""", """"event_simpleName":"""", """Written""" ]
  Fields = [
    """"timestamp":"({time}\d{10,13})"""",
    """"UserName":"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+)))""""
    """"aip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"name":"({event_name}[^"]+)"""",
    """"event_simpleName":"({event_code}[^"]+)"""",
    """"TargetFileName":"({file_path}(({file_dir}[^"]*?)[\\\/]+)?\s*({file_name}[^\\\/"]+?(\.(\d+|({file_ext}[^\\\/"\.]+)))?))"""",
    """"Size":"({bytes}\d+)"""",
    """"DiskParentDeviceInstanceId":"({device_id}[^"]{1,2099})"""",
    """"aid":"({aid}[^"]+)""""
    """"cid":"({cid}[^"]+)"""  
    """"event_platform":"({os}[^"]+)""""
  ]
  DupFields = [ "device_id->service_type" ]
  ParserVersion = v1.0.0


}
```