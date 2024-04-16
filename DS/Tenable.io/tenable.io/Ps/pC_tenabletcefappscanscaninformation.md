#### Parser Content
```Java
{
Name = tenable-t-cef-app-scan-scaninformation
  ParserVersion = v1.0.0
  Product = Tenable.io
  Vendor = Tenable.io
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"synopsys":""", """"pluginName":"Nessus Scan Information"""", """"pluginFamily":""" ]
  Fields = [
    """"synopsys":"({alert_name}[^",]+)""",
    """"pluginFamily":"({alert_type}[^",]+)"""",
# scan_name is removed
    """"severity":({alert_severity}\d+),""",
    """"description":"({additional_info}[^"]+)"""",
    """"assetIp":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"netBios":"({src_host}[^",]+)"""",
    """"pluginOutput":"({result}[^"]+?)\s*"""",
# start_scan_time is removed
# end_scan_time is removed
    """\Wdproc=(|({scan_type}.+?))(\s+\w+=|\s*$)""",
    """"os":"({os}[^",]+)""""
  ]
  DupFields = [ "start_scan_time->time" ]


}
```