#### Parser Content
```Java
{
Name = "crowdstrike-falcon-json-alert-trigger-success-eventsimplename"
Vendor = "CrowdStrike"
Product = "Falcon"
TimeFormat = "epoch_sec"
Conditions = [
""""event_simpleName":"ActiveDirectPrivilegeEscalation""""
]
Fields = [
""""timestamp":"({time}\d{10})"""
""""event_simpleName":\"({event_code}[^\"]+)"""
""""aid":"({aid}[^\"]+)"""
""""FalconHostLink\\*"+:\s*\\*\"+({falcon_host_link}[^\"]+)"""
""""cid":"({cid}[^"]+)"""
""""event_platform\\*":\\*"({os}[^"]+)\\*""""
]
DupFields = [
"event_code->alert_name"
"event_code->alert_type"
"falcon_host_link->additional_info"
]
ParserVersion = "v1.0.0"


}
```