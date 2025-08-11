#### Parser Content
```Java
{
Name = box-ccm-json-file-download-success-manageddevice
  Vendor = Box
  Product = Box Cloud Content Management
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"eventType":"DOWNLOADED"""", """"trustReason":"Download to a managed device"""", """"sourceName":"Box"""", """"fileName":"""", """"fileType":"FILE"""" ]
  Fields = [
    """"createTimestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3}Z)"""",
    """"fileName":"({file_name}[^"]+?(\.({file_ext}[^"\.]+))?)"""",
    """"filePath":"({file_dir}[^"]+)"""",
    """"fileType":"({file_type}[^"]+)"""",
    """"mimeTypeByBytes":"({mime}[^"]+)"""",
    """"eventType":"({operation}[^"]+)"""",
    """"deviceUserName":"({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""",
    """"operatingSystemUser":"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """"fileSize":({bytes}\d+),""",
    """"destinationName":"({dest_host}[\w\-\.]+)"""",
    """"privateIpAddresses":\["({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""",
    """"publicIpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""",
    """"md5Checksum":"({hash_md5}[^"]+)"""",
    """"sha256Checksum":"({hash_sha256}[^"]+)"""",
    """"trustReason":"({event_name}[^"]+)"""",
    """"title":"({additional_info}[^"]+)"""",
    """"tabUrl":"({url}[^"]+)"""",
    """"deviceUid":"({device_id}[^"]+)""""
  ]
  DupFields = [ "operation->access_type", "dest_host->device_name"]


}
```