#### Parser Content
```Java
{
Name = "cyberark-pam-str-app-activity-success-usepassword"
Vendor = "CyberArk"
Product = "CyberArk Privilege Access Manager"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
"""|Use Password|"""
"""|Operating System|"""
]
Fields = [
"""({time}\d+-\d+-\d+T\d+:\d+:\d+Z)\s+({host}[^\s]+)"""
"""Protocol=({protocol}[^\s;]+)"""
"""SessionID=({session_id}[^\s;]+)"""
"""SrcHost=({src_host}[^\s;]+)"""
"""User=(({domain}[^\\]*?)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""Command=({command}[^\s;,]+)"""
"""ProcessName =({process_name}[^\s;,]+)"""
"""DstHost=({dest_host}[^\s;,]+)"""
"""({time}\d+-\d+-\d+T\d+:\d+:\d+Z)\s+({host}[^\s]+)\s+\|({user}[\w\.\-\!\#\^\~]{1,40}\$?)\|[^\|]+\|({operation}[^\|]+)"""
]
ParserVersion = "v1.0.0"


}
```