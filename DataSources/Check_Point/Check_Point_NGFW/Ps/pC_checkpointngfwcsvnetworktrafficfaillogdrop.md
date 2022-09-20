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
    """({time}\d+\w+\d\d\d\d,\d+:\d+:\d+),(|({host}[^,]*)),log,({action}drop),([^,]*,){6}(|({rule}[^,]*)),[^,]*,(|({src_ip}[^,]*)),(|({dest_ip}[^,]*)),(|({protocol}[^,]*)),(|({dest_port}\d+)),(|({src_port}\d+)),([^,]*,){3}(|({src_translated_ip}[^,]*)),(|({dest_translated_ip}[^,]*)),([^,]*,){2}(|({dest_translated_port}\d*)),(|({src_translated_port}\d*)),([^,]*,){2}(|({user}[^,]*)),"""
  ]


}
```