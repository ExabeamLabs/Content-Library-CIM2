#### Parser Content
```Java
{
Name = cisco-securenwanalytics-json-network-session-success-flow_id
  Vendor = Cisco
  Product = Cisco Secure Network Analytics
  ParserVersion = "v1.0.0"
  TimeFormat =  "epoch"
  Conditions = [ """app_id":""", """inbound_packets":""", """flow_id":""", """firewall_action":""" ]
  Fields = [
        """"last_time"+:\s*({time}\d{13})"""
	""""service"+:\s*({service_name}\d+)"""
	""""protocol"+:\s*({protocol}\d+)"""
	""""service_id"+:\s*({service_id}\d+)"""
	""""client_ip_address":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
	""""server_ip_address":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
	""""inbound_bytes"+:\s*({bytes_in}\d+)"""
	""""inbound_packets"+:\s*({packets_in}\d+)"""
	""""outbound_bytes"+:\s*({bytes_out}\d+)"""
	""""outbound_packets"+:\s*({packets_out}\d+)"""
	""""ttl"+:\s*(null|({response_ttl}\d+))"""
        """"firewall_action"+:\s*(null|({action}\d+))"""
	""""total_bytes":\s*(null|({bytes}\d+))"""
  ]


}
```