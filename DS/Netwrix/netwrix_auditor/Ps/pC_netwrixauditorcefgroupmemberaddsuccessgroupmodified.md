#### Parser Content
```Java
{
Name = "netwrix-auditor-cef-group-member-add-success-groupmodified"
Vendor = "Netwrix"
Product = "Netwrix Auditor"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [
"""CEF:0|Netwrix|Active Directory|"""
"""|Modified group|"""
"""Added: """
]
Fields = [
"""start=({time}\w{3} \d\d \d\d\d\d \d\d:\d\d:\d\d)"""
"""suser=(N\/A|({email_address}[^@]+@[^\\\s]+)|(({domain}[^\\\s]+)\\+)?({user}[\w\.\-]{1,40}\$?)) """
"""shost=(unknown|({src_host}[^\s]+))"""
"""({app}Netwrix)"""
"""msg=({additional_info}.+?)(\s\w+=|$)"""
"""CEF:0\|Netwrix\|Active Directory\|[^\|]+\|[^\|]+\|({operation}[^\|]+)\|"""
"""cat=group.+?filePath=\\+?([^\\]+\\+)*?({group_name}[^\\]+) start="""
"""Added:.+?"+(\\+)?([^\\\/]+[\\\/]+)*?(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[\w\.\-]{1,40}\$?))(;|$|")"""
"""Group Type: "+({group_type}[^"]+)"+"""
]
ParserVersion = "v1.0.0"


}
```