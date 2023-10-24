#### Parser Content
```Java
{
Name = "qualys-q-json-app-activity-success-scan"
Vendor = "Qualys"
Product = "Qualys AssetView"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [ """"Severity":""",""""IP Address":""","""Last VM Scanned Date":""",""""Last Update Datetime":""" ]
Fields = [
  """"Last Update Datetime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""""
  """"Port":"(-|({src_port}\d+))""",
  """"Severity":({alert_severity}\d)"""
  """"Netbios Name":"({src_host}[\w\-.]+)""",
  """"IP Address":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
  """"Protocol":"(-|NaN|({protocol}[^"]+))"""",
  """"Status":"(NaN|-|({result}[^"]+))"""",
  """"Results":"(-|({additional_info}[^"]+))"""",
  """"QID":(-|({alert_id}\d+))""",
  """"Operating System":"({os}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```