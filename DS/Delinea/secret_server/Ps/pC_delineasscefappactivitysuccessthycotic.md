#### Parser Content
```Java
{
Name = "delinea-ss-cef-app-activity-success-thycotic"
Vendor = "Delinea"
Product = "Secret Server"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [ """|Thycotic Software|Secret Server|""", """Item Name:""" ]
Fields = [
"""\d{2}:\d{2}:\d{2} ({host}[\w\-.]+) CEF:"""
"""\srt=({time}\d+)"""
"""\srt=({time}\w+ \d{2} \d{4} \d{2}:\d{2}:\d{2})"""
"""\sdvc=({host}[^\s]+)"""
"""\sdvchost=({host}[^\s]+)"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s\w+="""
"""\ssuser=(({domain}[^\\\s]+?)(\\+))?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""\sduser=(({domain}[^\\\s]+?)(\\+))?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""({app}Thycotic Software)"""
"""\sfname=({object}[^=]+?)\s+\w+="""
"""\sContainer Name:\s*({resource}[^=]+?)\s*(?:\([^\)]*?\))?\s+(\w+=|\w+:|$)"""
"""Action:\s*\[({operation}[^\]]+)\]"""
"""\sfileType=({additional_info}[^=]+?)\s\w+="""
"""CEF:\s*\d+\|([^\|]+\|){4}({category}[^\|]+)"""
]
ParserVersion = "v1.0.0"


}
```