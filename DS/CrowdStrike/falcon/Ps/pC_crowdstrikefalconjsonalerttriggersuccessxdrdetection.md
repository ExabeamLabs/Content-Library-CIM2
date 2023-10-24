#### Parser Content
```Java
{
Name = "crowdstrike-falcon-json-alert-trigger-success-xdrdetection"
Vendor = "CrowdStrike"
Product = "Falcon"
ParserVersion = "v1.0.0"
TimeFormat = "epoch_sec"
Conditions = [ """"eventType":"XdrDetectionSummaryEvent"""", """"destinationServiceName":"CrowdStrike"""", """"Techniques":"""" ]
Fields = [
""""eventCreationTime":\s*({time}\d{10})"""
""""eventType":"({event_category}[^"]+)"""
""""destinationServiceName":"({app}.+?)"(\s+\w+=)?"""
"""Description":"({additional_info}[^"]+)""""
""""Severity":\s*({alert_severity}\d+),"""
""""DetectId":"({alert_id}[^"]+)""""
""""Tactics":"({category}[^"]+)""""
""""Techniques":"({alert_name}[^"]+)"""
""""Name":"({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|>]+))(?<!local)"""
""""DomainNames":"({domain}[^,]+)"""
""""IPv4Addresses":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""HostNames":"({host}[^,]+)"""
]
DupFields = [ "category->alert_type" ]


}
```