#### Parser Content
```Java
{
Name = ftp-f-str-app-activity-mkd
  Product = FTP
  ParserVersion = "v1.0.0"
  Conditions = [ """]mkd """ ]

s-common-ftp-app-activity = {
    Vendor = FTP
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Fields = [
	"""({host}[\w\.-]+)\s+(\S+\s+){2}\[\d+\]"""
	"""({src_ip}\S+)\s+(\S+\s+){2}\[\d+\]"""
	"""(-|(({domain}\S+)[\/\\])?({user}\S+))\s+\[\d+\]"""
	"""\[\d+\]({operation}\w+)\s+"""
	"""\[\d+\]\w+\s+({object}\S+)"""
	"""\[\d+\]\w+\s+(\S+\s+){2}({result}\d+)"""
	"""\[\d+\]\w+\s+(\S+\s+){4}({bytes}\d+)"""
    ]
    DupFields = [ "host->dest_host" 
}
```