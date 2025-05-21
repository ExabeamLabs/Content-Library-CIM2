#### Parser Content
```Java
{
Name = symantec-atp-json-alert-trigger-success-symcdeviceaction
  Vendor = Symantec
  Product = Symantec Advanced Threat Protection
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"app_name":""", """"symc_device_action":""", """"sep_mid":"""" ]
  Fields = [
    """"device_time":"({time}[^"]+)"""",
    """"user_name":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
    """"device_name":"({host}[^"]+)"""",
    """"categories":\["({alert_type}[^"]+)"""",
    """"signature_name":"({alert_name}[^"]+)"""",
    """severity":({alert_severity}\d+)""",
    """"host_name":"({src_host}[^"]+)"""",
    """event_id":({alert_id}\d+)""",
    """"app_name":"({malware_url}[^"]+)"""",
    """"domain_name":"({domain}[^"]+)"""",
    """"device_ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """"remote_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"data_source_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"event_desc":"({additional_info}[^"]+)"""",
    """app_name":"({file_path}(({file_dir}[^"\|]+)?[\\\/]+)?({file_name}[^\|"]+?))\s*""""
  ]


}
```