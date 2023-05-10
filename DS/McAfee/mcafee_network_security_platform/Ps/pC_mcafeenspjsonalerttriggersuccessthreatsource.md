#### Parser Content
```Java
{
Name = mcafee-nsp-json-alert-trigger-success-threatsource
  Vendor = McAfee
  Product = McAfee Network Security Platform
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = ["""threat_source_ip_address""" , """McAfee Host Intrusion Prevention"""]
  Fields = [
    """"event_generated_time":"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)""",
    """"action_taken":"({action}[^"]+)"""", 
    """"detecting_product_ipv4_address":"({host}[^"]+)"""",
    """"detecting_product_host_name":"({host}[^"]+)"""",
    """"threat_source_ip_address":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"threat_target_ip_address":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """"threat_source_user_name":"({domain}[^\\]+)\\+({user}[^"]+)"""",
    """"threat_severity":"({alert_severity}[^"]+)"""",
    """"threat_source_process_name":"\w+:\\+([^\\"]+\\+)+({process_name}[^"]+)"""",
    """"signature_name_host_ips":"({alert_name}[^"]+)"""",
    """"event_description":"({alert_type}[^"]+)"""",
    """"threat_source_host_name":"({src_host}[^"]+)"""",
    """"event_category":"({alert_type}[^"]+)"""",
    """"threat_target_host_name":"({dest_host}[^"]+)"""",
    """"threat_type":"({additional_info}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```