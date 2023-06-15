#### Parser Content
```Java
{
Name = microsoft-nps-csv-endpoint-login-success-ias-1
  Vendor = Microsoft
  Product = Microsoft Network Policy Server 
  TimeFormat = "MM/dd/yyyy,HH:mm:ss"
  Conditions = [ ""","IAS",""", """",2,"""" ]
  Fields = [
    """({host}[^"]+)","IAS",({time}\d\d\/\d\d\/\d\d\d\d,\d\d:\d\d:\d\d),(|({result}\d+)),(|"({user}[^"]+)"),([^,]*,){9}(|"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"),(|"({src_host}[^"]+)"),""",
    """"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?",[^,]*,\s*$""",
  ]
  ParserVersion = v1.0.0


}
```