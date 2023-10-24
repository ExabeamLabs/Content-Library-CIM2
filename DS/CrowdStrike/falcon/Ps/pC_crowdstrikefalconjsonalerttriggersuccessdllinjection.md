#### Parser Content
```Java
{
Name = "crowdstrike-falcon-json-alert-trigger-success-dllinjection"
Vendor = "CrowdStrike"
Product = "Falcon"
TimeFormat = "epoch"
Conditions = [
""""event_simpleName":"DllInjection""""
""""timestamp":""""
]
Fields = [
""""timestamp":\s*"*({time}\d{13})""""
"""\Whostname=(|({host}[^,=]+?)),?(\s+\w+=|\s*\})"""
""""InjectedDll":"({malware_file_name}[^"]+)"""
""""event_simpleName":"({alert_name}[^"]+)"""
""""id":"({alert_id}[^"]+)"""
""""aid":"({aid}[^"]+)"""
""""cid":"({cid}[^"]+)"""
""""event_platform":"({os}[^"]+)""""
]
DupFields = [
"alert_name->alert_type"
"alert_name->event_code"
"alert_name->alert_subject"
]
ParserVersion = "v1.0.0"


}
```