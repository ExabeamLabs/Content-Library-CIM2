#### Parser Content
```Java
{
Name = "stealthbits-s-cef-file-read-success-filemonitor"
Vendor = "StealthBits"
Product = "StealthIntercept"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
Conditions = [
"""|STEALTHbits|SBTService|"""
"""|FileMonitor|"""
"""Operation="""
]
Fields = [
"""\s+({host}[\w.\-]+)\s+CEF:"""
"""\Wrt=({time}\d+\-\d+\-\d+ \d+:\d+:\d+\.\d+)"""
"""\Wsntdom=({domain}[^\s]+)"""
"""\Wsuser=(({domain}[^\\]+)\\)?({user}[\w\.\-]{1,40}\$?)"""
"""\Wsrc=(|({process_name}.+?))(\s+\w+=|\s*$)"""
"""\Wduser=(|({file_path}({file_dir}.+?)(\\({file_name}[^\\]+?))?))(\s+\w+=|\s*$)"""
"""\Wshost=(|({dest_host}.+?))(\s+\w+=|\s*$)"""
"""\WSuccess=\s*(|({result}.+?))(\s+\w+=|\s*$)"""
"""\WBlocked=\s*(|({blocked}[^\s]+))\sAttribute"""
"""\WOperation=\s*(null|({access}[\s\w]+?))\s*(\d{4}\-|"|$|\w+=)"""
]
ParserVersion = "v1.0.0"


}
```