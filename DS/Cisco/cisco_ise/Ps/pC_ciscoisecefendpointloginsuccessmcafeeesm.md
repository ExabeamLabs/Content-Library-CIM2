#### Parser Content
```Java
{
Name = "cisco-ise-cef-endpoint-login-success-mcafeeesm"
Vendor = "Cisco"
Product = "Cisco ISE"
TimeFormat = "epoch"
Conditions = [
  """|McAfee|ESM"""
  """|268-2146859015|"""
]
Fields = [
  """\srt=({time}\d{13})"""
  """deviceTranslatedAddress=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """src=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """suser=({user}[\w\.\-]{1,40}\$?)\s+nitroSensor_Name"""
  """nitroSensor_Name =({auth_server}[^\s]+)"""
]
ParserVersion = "v1.0.0"


}
```