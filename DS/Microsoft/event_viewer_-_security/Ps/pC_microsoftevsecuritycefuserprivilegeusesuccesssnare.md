#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-user-privilege-use-success-snare"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|Snare|"""
"""|Security:578|Privileged object operation|"""
]
Fields = [
"""\srt=({time}\d{13})"""
"""CEF:([^\|]*\|){4}Security:({event_code}\d+)\|({event_name}[^\|]+)"""
"""\scategoryBehavior=(|({action}.+?))(\s+\w+=|\s*$)"""
"""\scategoryOutcome=(|/({result}.+?))(\s+\w+=|\s*$)"""
"""\scategoryObject=(|({object}.+?))(\s+\w+=|\s*$)"""
"""\sdhost=(|({dest_host}[\w\-.]+?))(\s+\w+=|\s*$)"""
"""\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\sduser=(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\w+=|\s*$)"""
"""Process ID\\=({process_id}\d+)"""
"""Primary User Name\\=(-|NETWORK SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""Primary Domain\\=(-|({domain}[^=&]+))"""
"""Primary Logon ID\\=(-|({login_id}[^=&]+))"""
"""Privileges\\=(-|({privileges}[^=&]+))"""
"""User\\=(-|NETWORK SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""ComputerName\\=({host}[\w.\-]+)"""
]
ParserVersion = "v1.0.0"


}
```