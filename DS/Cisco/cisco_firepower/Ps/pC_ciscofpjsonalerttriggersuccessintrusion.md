#### Parser Content
```Java
{
Name = "cisco-fp-json-alert-trigger-success-intrusion"
Vendor = "Cisco"
Product = "Cisco Firepower"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """"originator_type":"FTD"""",
  """"intrusion_rule_message":"""
]
Fields = [
""""event_second":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""""
""""severity":({alert_severity}\d+)"""
""""application_id":({app_id}\d+)"""
""""context":"({additional_info}[^"]+)""""
""""device":"({dest_host}[^"]+)""""
""""device_ip":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
""""device_uuid":"({device_id}[^"]+)""""
""""egress_interface":"({src_interface}[^"]+)""""
""""egress_zone":"({egress_zone}[^"]+)""""
""""firewall_policy":"({policy_name}[^"]+)""""
""""firewall_rule":"({rule}[^"]+)""""
""""ingress_interface":"({src_interface}[^"]+)""""
""""ingress_zone":"({ingress_zone}[^"]+)""""
""""initiator_country_code":"({src_country}[^"]+)""""
""""initiator_ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
""""initiator_port":({src_port}\d+)"""
""""intrusion_policy":"({policy_name}[^"]+)""""
""""protocol":"({protocol}[^"]+)""""
""""responder_country_code":"({dest_country}[^"]+)""""
""""responder_ip":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
""""responder_port":({dest_port}\d+)"""
""""user_full_name":"({full_name}[^"]+)""""
""""username":"({user}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```