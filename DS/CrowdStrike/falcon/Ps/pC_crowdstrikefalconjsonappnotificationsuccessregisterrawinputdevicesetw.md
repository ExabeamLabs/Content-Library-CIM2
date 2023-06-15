#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-app-notification-success-registerrawinputdevicesetw
  ParserVersion = v1.0.0
  Conditions = [ """"destinationServiceName":"CrowdStrike"""", """"event_simpleName":"RegisterRawInputDevicesEtw"""", """"event_platform":"""" ]

crowdstrike-json-app-notification = {
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "epoch"
  Fields = [
    """"eventCreationTime":({time}\d{13})""",
    """"timestamp":\s*"*({time}\d{13})""",
    """"aid":\s*"({aid}[^"]+)""",
    """"UserName":\s*"({user}[^"]+?)""""
    """"aip":\s*"({aip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
    """"name":\s*"({alert_type}[^"]+)"""
    """"ClientComputerName":\s*"({src_host}[^"]+)"""
    """"event_platform":\s*"({os}[^"]+)""",
    """"UserSid":\s*"({user_sid}[^"]+)""",
    """"RemoteAddressIP4":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """"destinationServiceName":"({app}CrowdStrike)""""
  
}
```