#### Parser Content
```Java
{
Name = ftp-f-str-app-activity-sshdisconnect
  ParserVersion = "v1.0.0"
  Product = FTP
  Conditions = [ """]ssh_disconnect """ ]

s-common-ftp-app-activity = {
    Vendor = FTP
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Fields = [
	"""({host}[\w\.-]+)\s+(\S+\s+){2}\[\d+\]"""
	"""({src_ip}\S+)\s+(\S+\s+){2}\[\d+\]"""
	"""(-|(({domain}\S+)[\/\\])?({user}[\w\.\-]{1,40}\$?))\s+\[\d+\]"""
	"""\[\d+\]({operation}\w+)\s+"""
	"""\[\d+\]\w+\s+({object}\S+)"""
	"""\[\d+\]\w+\s+(\S+\s+){2}({result}\d+)"""
	"""\[\d+\]\w+\s+(\S+\s+){4}({bytes}\d+)"""
    ]
    DupFields = [ "host->dest_host" 
}
```