#### Parser Content
```Java
{
Name = crowdstrike-falcon-sk4-alert-trigger-suspiciousdnsrequest
   Vendor = CrowdStrike
   ParserVersion = "v1.0.0"
   Product = Falcon
   TimeFormat = "epoch_sec"
   Conditions = [ """"event_simpleName":"SuspiciousDnsRequest"""" ]
   Fields = [
     """"aip":"({host}[^"]+)"""
     """"timestamp":"({time}\d{10})""",
     """"DomainName":"({domain}[^"]+)""",
     """"event_simpleName":"({event_code}[^"]+)""",
     """"aid":"({aid}[^"]+)"""
    ]
    DupFields = ["event_code->alert_name", "event_code->alert_type"]


}
```