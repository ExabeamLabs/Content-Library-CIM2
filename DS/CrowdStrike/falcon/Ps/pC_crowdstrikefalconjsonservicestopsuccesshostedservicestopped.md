#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-service-stop-success-hostedservicestopped
  Vendor = CrowdStrike
  Product = Falcon
  ParserVersion = v1.0.0
  TimeFormat = "epoch"
  Conditions = [ """"event_simpleName":"HostedServiceStopped"""", """"destinationServiceName":"CrowdStrike"""" ]
  Fields = [
    """timestamp":"({time}\d{13})"""
    """"event_simpleName":"({event_name}[^"]+)"""",
    """"aip":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""",
    """"event_platform":"({os}[^"]+)"""",
    """"ServiceDisplayName":"({service_name}[^"]+)""""
  ]


}
```