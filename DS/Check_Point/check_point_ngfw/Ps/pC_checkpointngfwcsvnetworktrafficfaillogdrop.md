#### Parser Content
```Java
{
Name = checkpoint-ngfw-csv-network-traffic-fail-logdrop
  ParserVersion = v1.0.0
  Vendor = Check Point
  Product = Check Point NGFW
  TimeFormat = "ddMMMyyyy','HH:mm:ss"
  Conditions = [ """,log,drop,""" ]
  Fields = [
    """({time}\d+\w+\d\d\d\d,\d+:\d+:\d+),(|({host}[^,]*)),log,({action}drop),([^,]*,){6}(|({rule}[^,]*)),[^,]*,(|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?),(|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?),(|({protocol}[^,]*)),(|({=dest_port}\d+)),(|({=src_port}\d+)),([^,]*,){3}(|({src_translated_ip}[^,]*)),(|({dest_translated_ip}[^,]*)),([^,]*,){2}(|({dest_translated_port}\d*)),(|({src_translated_port}\d*)),([^,]*,){2}(|({user}[^,]*)),"""
  ]


}
```