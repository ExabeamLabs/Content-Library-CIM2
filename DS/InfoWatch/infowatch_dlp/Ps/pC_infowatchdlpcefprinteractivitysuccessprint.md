#### Parser Content
```Java
{
Name = "infowatch-dlp-cef-printer-activity-success-print"
Vendor = "InfoWatch"
Product = "InfoWatch DLP"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|Print|"""
"""|DLP|DLP TM"""
]
Fields = [
"""({operation}Print)"""
"""\Wact=({result}.+?)(\s+[\w\.]+=|\s*$)"""
"""\Wrt=({time}\d{13})"""
"""\Wshost=({src_host}.+?)(\s+[\w\.]+=|\s*$)"""
"""\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wsntdom=({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^@]+?)(\s+[\w\.]+=|\s*$)"""
"""\Wsuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+[\w\.]+=|\s*$)"""
"""\Wsuid=({full_name}.+?)(\s+[\w\.]+=|\s*$)"""
"""\Wfname=({object}.+?)(\s+[\w\.]+=|\s*$)"""
"""\Wdvchost=({host}.+?)(\s+[\w\.]+=|\s*$)"""
"""\Wcs3=({additional_info}.+?)(\s+[\w\.]+=|\s*$)"""
"""\Wad\.categories=({categories}.+?)(\s+[\w\.]+=|\s*$)"""
"""\Wad\.fingerprints=({fingerprints}.+?)(\s+[\w\.]+=|\s*$)"""
"""\Wad\.device__name=({printer_name}.*?({dest_host}[^\\\/]+?))(\s+[\w\.]+=|\s*$)"""
]
DupFields = [
"object->file_name"
]
ParserVersion = "v1.0.0"


}
```