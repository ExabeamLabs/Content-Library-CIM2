#### Parser Content
```Java
{
Name = pan-ngfw-json-network-notification-success-iptag
  Vendor = Palo Alto Networks
  Product = GlobalProtect
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [  """LogType":"IPTAG""", """TagName":""", """"MappingDataSource":""", """"SourceIP":""" ]
  Fields = [
  """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,6}Z)"""
  """"DeviceName":"({host}[\w\-\.]+)"""
  """"TagName":"({tag}[^"]+)""""
  """"MappingDataSource":"({additional_info}[^"]+)""""
  """"SourceIP":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""  
   ]
  ParserVersion = "v1.0.0"


}
```