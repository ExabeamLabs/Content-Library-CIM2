#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-file-write-success-written
  Vendor = CrowdStrike
  Product = Falcon
  ParserVersion = v1.0.0
  TimeFormat = "epoch"
  Conditions = [ """"destinationServiceName":"CrowdStrike"""" ,""""IsOnRemovableDisk":"1"""", """"event_simpleName":""", """Written"""" ]
  Fields = [
    """"timestamp":"({time}\d{13})"""",
    """"UserName":"({user}[^"]+)"""",
    """"aip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"name":"({event_name}[^"]+)"""",
    """"event_simpleName":"({event_code}[^"]+)"""",
    """"TargetFileName":"({file_path}(({file_dir}[^"]*?)[\\\/]+)?\s*({file_name}[^\\\/"]+?(\.(\d+|({file_ext}[^\\\/"\.]+?)))?))\s*"""",
    """"Size":"({bytes}\d+)"""",
    """"DiskParentDeviceInstanceId":"({device_id}[^"]+)"""",
    """"aid":"({aid}[^"]+)""""
    """"aip":"({aip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
    """"((?i)SHA256String|SHA256HashData)":"({hash_sha256}[^"]+)""""
    """"ContextProcessId":"({process_guid}[^"]+)""""
    """"ShareAccess":"({access}[^"]+)""""
  ]
  DupFields = [ "device_id->service_type" ]


}
```