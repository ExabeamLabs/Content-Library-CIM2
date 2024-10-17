#### Parser Content
```Java
{
Name = "vmware-carbonblackedr-leef-alert-trigger-success-watchliststoragehitprocess"
Vendor = "VMware"
Product = "Carbon Black EDR"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""LEEF:"""
"""|CB|"""
"""watchlist.storage.hit.process"""
"""process_name="""
]
Fields = [
"""\Wstart=({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)\s"""
"""\Wusername=((({domain}[^\\\s]+)\\\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""\Wprocess_name=({process_name}[^=]+?)\s*(([\w_]+=)|$)"""
"""\Wpath=({process_path}({process_dir}[^=]*?[\\\/]+)?[^\\\/=]+?)(\s+\w+=|\s*$)"""
"""\Wtype=({alert_name}watchlist.storage.hit.process)"""
"""\Wwatchlist_name=({alert_name}[^=]+?)(\s+\w+=|\s*$)"""
"""\Wtype=({alert_type}watchlist.storage.hit.process)"""
"""\Wcmdline=(|({process_command_line}.+?))(\s+\w+=|\s*$)"""
"""\Wprocess_pid=({process_id}[^\s]+)"""
]
ParserVersion = "v1.0.0"


}
```