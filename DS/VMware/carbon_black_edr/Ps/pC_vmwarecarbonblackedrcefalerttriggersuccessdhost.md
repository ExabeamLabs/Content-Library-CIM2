#### Parser Content
```Java
{
Name = "vmware-carbonblackedr-cef-alert-trigger-success-dhost"
Vendor = "VMware"
Product = "Carbon Black EDR"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|Carbon Black|Carbon Black|"""
"""|reason="""
"""dhost="""
]
Fields = [
"""\|reason=({alert_type}.+?)\|({alert_name}.+?)\|({alert_severity}\d+)?"""
"""\srt=({time}\d{13})"""
"""\sdhost=({src_host}[^\s]+)"""
"""\s(dst|local_ip)=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sdeviceSeverity=({alert_severity}\d+)"""
"""\sdirection:({direction}(Inbound|Outbound))"""
"""\sremote_ip:({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\salliance_link_[^\s:]+:({additional_info}[^\s]+)"""
"""\sfname=({malware_url}.+?)\s+\w+="""
"""\sfname=({malware_url_path}\w+:\/\/.+?)\s+\w+="""
"""\sfname=({file_path}(?!\w+:\/\/).+?)\s+\w+="""
"""\sdvchost=({host}[^\s]+)"""
"""\sdproc=({process_name}.*?)\s\w+="""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```