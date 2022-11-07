#### Parser Content
```Java
{
Name = crowdstrike-falcon-sk4-app-notification-fdr
  Vendor = CrowdStrike
  Product = Falcon
  ParserVersion = v1.0.0
  TimeFormat = "epoch_sec"
  Conditions = [ """"timestamp":"""", """requestClientApplication=FDR""" ]
  Fields = [
    """"ComputerName":"({host}[^"]+)"""",
    """"event_simpleName":"({event_name}[^"]+)"""",
    """"timestamp":"({time}\d{10})"""",
    """"event_platform":"({os}[^"]+)"""",
    """"aip":"({src_ip}[^"]+)"""",
    """"aid":"({agent_id}[^"]+)"""",
    """"TargetFileName":"({file_name}[^"]+)"""",
    """"DownloadPath":"({file_path}[^"]+)"""",
    """"DomainName":"({domain}[^"]+)"""",
  ]
  DupFields = ["host->dest_host"]


}
```