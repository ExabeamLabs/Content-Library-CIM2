#### Parser Content
```Java
{
Name = tanium-cp-sk4-alert-trigger-success-taniumindex
  Vendor = Tanium
  Product = Tanium Core Platform
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"Intel Name":"Vulnerable Log4j MD5 Hashes"""", """"source":"tanium-index"""", """"MITRE Techniques":"""" ]
  Fields = [
    """"Timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)"""",
    """"Computer Name":"({src_host}[^"]+?)"""",
    """"Computer IP":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"Intel Id":({alert_id}\d+)""",
    """"Intel Type":"({alert_type}[^"]+)"""",
    """"Intel Name":"({alert_name}[^"]+)"""",
    """"source":"({log_source}[^"]+)"""",
    """properties":\{"fullpath":"({process_path}({process_dir}[^"]+?)\\+({process_name}[^"\\]+))""""
  ]


}
```