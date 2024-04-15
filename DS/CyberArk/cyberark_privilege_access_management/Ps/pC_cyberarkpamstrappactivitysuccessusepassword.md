#### Parser Content
```Java
{
Name = "cyberark-pam-str-app-activity-success-usepassword"
Vendor = "CyberArk"
Product = "Cyberark Privilege Access Management"
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
"""User=(({domain}[^\\]*?)\\+)?({user}[^\s;]+)"""
"""Command=({command}[^\s;,]+)"""
"""ProcessName =({process_name}[^\s;,]+)"""
"""DstHost=({dest_host}[^\s;,]+)"""
"""({time}\d+-\d+-\d+T\d+:\d+:\d+Z)\s+({host}[^\s]+)\s+\|({user}[^\|]+)\|[^\|]+\|({operation}[^\|]+)"""
]
ParserVersion = "v1.0.0"


}
```