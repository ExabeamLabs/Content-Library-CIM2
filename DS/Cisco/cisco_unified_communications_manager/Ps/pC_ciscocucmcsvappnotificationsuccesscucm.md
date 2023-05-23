#### Parser Content
```Java
{
Name = cisco-cucm-csv-app-notification-success-cucm
  Vendor = Cisco
  Product = Cisco Unified Communications Manager
  TimeFormat = "epoch_sec"
  Conditions = [ ""","CUCM-Cluster",""", ]
  Fields = [
    """({event_code}1),({callmanager_id}\d+),({call_id}\d+),[^,]*,({time}\d{10}),([^,]*,){4}"?(|({user}[^",]+))"?,([^,]*,){21}"?(|({dest_user}[^",]+))"?,([^,]*,){23}({duration}\d+),"?({src_host}[\w.-]+)"?,"?(|({dest_host}[^"]+))"?,([^,]*,){7}"CUCM-Cluster",[^,]*,"?(|({additional_info}[^",]+))"?,([^,]*,){12}"?(\s*|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"?,"?(\s*|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"?,([^,]*,){12}({protocol}\d+),"""
    """({event_code}2),({callmanager_id}\d+),({call_id}\d+),([^,]*,){3}({time}\d{10}),(|({packets_out}\d*)),[^,]*,(|({packets_in}\d+)),([^,]*,){2}({jitter}[^,]+),({latency}[^,]+),([^,]*,){2}"CUCM-Cluster","?({host}[^",]+)"?,"?(|({additional_info}[^"]+))"?,(|({duration}\d+)),"""
  ]
  ParserVersion = "v1.0.0"


}
```