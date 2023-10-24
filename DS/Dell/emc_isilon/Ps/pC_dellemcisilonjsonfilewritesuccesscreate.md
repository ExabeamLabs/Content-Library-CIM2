#### Parser Content
```Java
{
Name = "dell-emcisilon-json-file-write-success-create"
Vendor = "Dell"
Product = "EMC Isilon"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [ """"SMB2"""" , """eventType""" , """"create"""" ]
Fields = [
  """({time}\d+-\d+-\d+T\d+:\d+:\d+[\+\-]\d+:\d+)\s+({host}[\w\-.]+)\s+.+?protocol[\":]+({protocol}[^\"]+)[\",]+zoneID[\":]+({zone_id}[\d]+)[,\"]+zoneName[:\"]+[^\"]+[\",]+eventType[\":]+({access}[^\"]+)[\",]+createResult[\":]+({result}[^\"]+).+?clientIPAddr[\":]+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?[\",]+userSID[\":]+({user_sid}[^\"]+)[\",]+userID[\":]+({user}[\w\.\-]{1,40}\$?)[,\"]+"""
  """\"fileName\"*:\"*({file_path}(({file_dir}[^\"]+)[\\\/]+)?(({file_name}[^\"\\\/]+?(\.({file_ext}[^\.\"]+))?)))\"*,"""
]
ParserVersion = "v1.0.0"


}
```