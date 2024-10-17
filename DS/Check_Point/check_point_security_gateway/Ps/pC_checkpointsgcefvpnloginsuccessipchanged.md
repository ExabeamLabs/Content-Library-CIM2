#### Parser Content
```Java
{
Name = "checkpoint-sg-cef-vpn-login-success-ipchanged"
Vendor = "Check Point"
Product = "Check Point Security Gateway"
TimeFormat = "epoch"
Conditions = [
"""|Check Point|Connectra|"""
"""|ip changed|"""
]
Fields = [
"""\srt=({time}\d{13})(\s+[\w\.:]+=|$)"""
"""\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(\s+[\w\.:]+=|$)"""
"""\sdvchost=({host}.+?)(\s+[\w\.:]+=|$)"""
"""\sduser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+[\w\.:]+=|$)"""
"""\sduser=[^=]+?\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)\)(\s+[\w\.:]+=|$)"""
"""\sshost=({src_host}.+?)(\s+[\w\.:]+=|$)"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?(\s+[\w\.:]+=|$)"""
"""\sad.os__name=({os}.+?)(\s+[\w\.:]+=|$)"""
"""\sad.assigned__IP:=({src_translated_ipnum}.+?)(\s+[\w\.:]+=|$)"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```