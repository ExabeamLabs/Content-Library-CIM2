#### Parser Content
```Java
{
Name = symantec-edr-json-alert-trigger-success-symcdeviceaction
  Vendor = Symantec
  Product = Symantec EDR
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"app_name":""", """"symc_device_action":""", """"sep_mid":"""" ]
  Fields = [
    """"device_time":"({time}[^"]+)"""",
    """"user_name":"({user}[^"]+)"""",
    """"device_name":"({host}[^"]+)"""",
    """"categories":\["({alert_type}[^"]+)"""",
    """"signature_name":"({alert_name}[^"]+)"""",
    """severity":({alert_severity}\d+)""",
    """"host_name":"({src_host}[^"]+)"""",
    """event_id":({alert_id}\d+)""",
    """"app_name":"({malware_url}[^"]+)"""",
    """"domain_name":"({domain}[^"]+)"""",
    """"device_ip":"({dest_ip}[^"]+)"""",
    """"remote_ip":"({src_ip}[^"]+)"""",
    """"data_source_ip":"({src_ip}[^"]+)"""",
    """"event_desc":"({additional_info}[^"]+)"""",
    """app_name":"({file_path}(({file_dir}[^"\|]+)?[\\\/]+)?({file_name}[^\|"]+?))\s*""""
  ]


}
```