#### Parser Content
```Java
{
Name = "checkpoint-sg-cef-vpn-login-success-authcrypt"
Vendor = "Check Point"
Product = "Check Point Security Gateway"
TimeFormat = "epoch"
Conditions = [
"""|Check Point|Connectra|"""
"""|authcrypt|"""
]
Fields = [
"""\srt=({time}\d{13})(\s+[\w\.:]+=|$)"""
"""\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(\s+[\w\.:]+=|$)"""
"""\sdvchost=({host}.+?)(\s+[\w\.:]+=|$)"""
"""\sad.User=({user}.+?)(\s+[\w\.:]+=|$)"""
"""\sad.User=[^=]+?\(({user}[^\(\)]+)\)(\s+[\w\.:]+=|$)"""
"""\sshost=({src_host}.+?)(\s+[\w\.:]+=|$)"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?(\s+[\w\.:]+=|$)"""
"""\sad.os__name=({os}.+?)(\s+[\w\.:]+=|$)"""
"""\sad.office__mode__ip=({src_translated_ipnum}.+?)(\s+[\w\.:]+=|$)"""
]
DupFields = [
"host->dest_host"
"user->account"
]
ParserVersion = "v1.0.0"


}
```