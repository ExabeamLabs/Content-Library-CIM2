#### Parser Content
```Java
{
Name = "blackberry-protect-cef-alert-trigger-success-cylance"
Vendor = "BlackBerry"
Product = "BlackBerry Protect"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|Cylance|PROTECT|"""
"""eventId="""
]
Fields = [
"""\Wdvchost=({host}[\w\-.]+)"""
"""\Wrt=({time}\d{13})"""
"""\WeventId=({alert_id}\d+)"""
"""\Wdhost=({dest_host}[\w\-.]+)"""
"""\Wdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\Wduser=\(?((({domain}[^\\\s\(\),]+)\\+)?(SYSTEM|({user}[^\\\s\(\),]+)))[^\)]*\)?\s"""
"""CEF:([^\|]*\|){6}(Unknown|({alert_severity}[^\|]+))"""
"""CEF:([^\|]*\|){5}({alert_name}[^\|]+)"""
"""\Wcs4=({alert_name}.+?)\s+(\w+=|$)"""
"""\WfilePath=(|({malware_url}.+?))\s+(\w+=|$)"""
"""\Wmsg=(|({additional_info}.+?))\s+(\w+=|$)"""
"""\Wact=(|({action}.+?))\s+(\w+=|$)"""
"""\Wad\.Process_,Name =(|({process_path}({process_dir}(?:(\w+:)*([\\\/]+[^\\\/"]+?)+?)?[\\\/]+)({process_name}[^"\\\/]+?)))\s+(\w+=|$)"""
]
DupFields = [
"alert_name->alert_type"
]
ParserVersion = "v1.0.0"


}
```