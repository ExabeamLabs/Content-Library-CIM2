#### Parser Content
```Java
{
Name = microsoft-nps-csv-endpoint-login-success-ias-1
  Vendor = Microsoft
  Product = Network Policy Server 
  TimeFormat = "MM/dd/yyyy,HH:mm:ss"
  Conditions = [ ""","IAS",""", """",2,"""" ]
  Fields = [
    """({host}[^"]+)","IAS",({time}\d\d\/\d\d\/\d\d\d\d,\d\d:\d\d:\d\d),(|({action}\d+)),(|"({user}[^"]+)"),([^,]*,){9}(|"({src_ip}[^"]+)"),(|"({src_host}[^"]+)"),""",
    """"({dest_ip}[^"]+)",[^,]*,\s*$""",
  ]
  ParserVersion = v1.0.0


}
```