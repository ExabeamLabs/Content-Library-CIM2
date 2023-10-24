#### Parser Content
```Java
{
Name = "crowdstrike-falcon-sk4-alert-trigger-success-quarantinedfilestate"
Vendor = "CrowdStrike"
Product = "Falcon"
TimeFormat = "epoch_sec"
Conditions = [
""""event_simpleName":"QuarantinedFileState""""
"""QuarantinedFileName":""""
]
Fields = [
""""timestamp":"({time}\d{10})"""
""""event_simpleName":"({alert_name}[^"]+)"""
""""aip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""aid":"({aid}[^"]+)"""
""""event_platform":"({os}[^"]+)"""
""""ConfigStateHash":"({old_hash}[^"]+)"""
""""SHA256HashData":"({new_hash}[^"]+)"""
""""ImageFileName":"({file_path}[^"]+)"""
""""ImageFileName":"({file_dir}[^"]*[\\\/]+)({file_name}[^\\\/"]+?\.({file_ext}[^\\\.\s"]+)?)""""
""""cid":"({cid}[^"]+)"""
]
DupFields = [
"alert_name->alert_type",
"alert_name->alert_subject"
]
ParserVersion = "v1.0.0"


}
```