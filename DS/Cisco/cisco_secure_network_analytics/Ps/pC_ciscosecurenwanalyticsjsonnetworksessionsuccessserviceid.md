#### Parser Content
```Java
{
Name = cisco-securenwanalytics-json-network-session-success-serviceid
  Vendor = Cisco
  Product = Cisco Secure Network Analytics
  ParserVersion = "v1.0.0"
  TimeFormat =  "epoch"
  Conditions = [ """app_id":""", """protocol":""", """service_id":""", """nbar_app_id":"""  ]
  Fields = [
    """"start_time"+:\s*({time}\d{13})"""
    """"service"+:\s*({service_name}\d+)"""
    """"protocol"+:\s*({protocol}\d+)"""
    """"service_id"+:\s*({service_id}\d+)"""
    """"endpoint2_port"+:\s*({src_port}\d+)"""
    """"endpoint1_port"+:\s*({dest_port}\d+)"""
    """"protocol"+:\s*({protocol}\d+)"""
    """"service_id"+:\s*({service_id}\d+)"""
    """"endpoint1_bytes"+:\s*({bytes_out}\d+)"""
    """"app_id":\s*({app_id}\d+)"""
    """"username"+:\s*"({user}[^",]+)"""
    """"endpoint2_packets"+:({bytes_in}\d+)"""
    """"endpoint1_ip_address"+:\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
    """"endpoint2_mac_address"+:\s*"({src_mac}[^",]+)"""
    """"endpoint1_ip_address"+:\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
    """"endpoint1_mac_address"+:\s*"({dest_mac}[^",]+)"""
    """"endpoint2_ip_address"+:\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  ]


}
```