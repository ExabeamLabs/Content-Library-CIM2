#### Parser Content
```Java
{
Name = cisco-fp-json-alert-trigger-success-502
  Vendor = Cisco
  Product = Cisco Firepower
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch_sec"
  Conditions = [ """"protocol":""", """"recordType": 502,""", """blockLength""", """"recordTypeDescription":""" ]
  Fields = [
    """"connectionTimestamp":\s+({time}\d{10})""",
    """"sensor":\s+"({host}[^"]+)"""",
    """"sourceIpAddress":\s+"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"destinationIpAddress":\s+"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"fileSize":\s+({bytes}\d+)""",
    """"recordTypeDescription":\s+"({alert_name}[^"]+)"""",
    """"filePolicy":\s+"({rule}[^"]+)"""",
    """"destinationPort":\s+({dest_port}\d+)""",
    """"sourcePort":\s+({src_port}\d+)""",
    """"clientApplication":\s+"({process_path}[^"]+)"""",
    """"shaHash":\s+"({hash_md5}[^"]+)"""",
    """"uri":.+?"data":\s+"({malware_url}[^"]+)"""",
    """"fileName":.+?"data":\s+"({malware_file_name}[^"]+)"""",
    """"direction":\s+({direction}[^,]+),""",
    """"fileType":\s+"({file_type}[^"]+)"""",
    """"user":\s+"(No Authentication Required|Unknown|({user}[\w\.\-]{1,40}\$?))"""",
    """"disposition"+:\s+({result}\d+)""",
    """"disposition"+:\s+"+(N\/A|Unknown|({additional_info}[^"]+))"""",
    """"threatScore"+:\s+({alert_severity}\d+)""",
    """"recordType"+:\s+({record_type}\d+)"""
  ]
  DupFields = [ "alert_name->alert_type" , "process_path->process_name"]


}
```