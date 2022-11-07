#### Parser Content
```Java
{
Name = nasuni-n-csv-file-permission-modify-success-dosattribute
	Product = Nasuni
    Conditions = [ """,CIFS,""", """,Set DOS Attribute,""" ]
	ParserVersion = v1.0.0
  
s-nasuni-file-operations = {
  Vendor = Nasuni
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Fields = [
    """({access}[^,]+),([^,]*,){2}(({domain}[^,\\]+)[\\]+)?({user}[^,\\]+),([^,]*,){2}("[^"]+"|[^,]*),[^,]*,({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """({file_dir}[^,]+\/+)?({file_name}[^,\/]+),[^,]+,([^,"]*,){3}("[^"]+"|[^,]*),CIFS,""",
    """({file_path}[^,]+),([^,"]*,){4}("[^"]+"|[^,]*),CIFS,""",
    """(({file_dir}[^,]+)[\/]+)?({file_name}[^\/,]+?(\.({file_ext}[^\/,\.]+))?),([^,"]*,){4}("[^"]+"|[^,]*),CIFS,""",
    """({file_path}[^,]+),([^,"]*,){3}("[^"]+"|[^,]*),CIFS,""",
    """(({file_dir}[^,]+)[\/]+)?({file_name}[^\/,]+?(\.({file_ext}[^\/,\.]+))?),([^,"]*,){3}("[^"]+"|[^,]*),CIFS,""",
  ]
  DupFields = [ "host->dest_host" 
}
```