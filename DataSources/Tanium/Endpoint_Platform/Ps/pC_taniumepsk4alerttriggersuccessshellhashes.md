#### Parser Content
```Java
{
Name = tanium-ep-sk4-alert-trigger-success-shellhashes
  Vendor = Tanium
  Product = Endpoint Platform
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"Intel Name":"CVE-2021-44228-Log4Shell-Hashes"""", """"source":"tanium-index"""", """"MITRE Techniques":"""" ]
  Fields = [
    """"Timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)"""",
    """"Computer Name":"({src_host}[^"]+?)"""",
    """"Computer IP":"({src_ip}[a-fA-F\d\.:]+)"""",
    """"Intel Id":({alert_id}\d+)""",
    """"Intel Type":"({alert_type}[^"]+)"""",
    """"Intel Name":"({alert_name}[^"]+)"""",
    """"source":"({log_source}[^"]+)"""",
    """properties":\{"fullpath":"({process_path}({process_dir}[^"]+?)\\+({process_name}[^"\\]+))""""
  ]


}
```