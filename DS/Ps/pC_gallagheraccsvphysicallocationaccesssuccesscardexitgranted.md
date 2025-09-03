#### Parser Content
```Java
{
Name = "gallagher-ac-csv-physical-location-access-success-cardexitgranted"
Conditions = [
  """gallagher"""
  """Card Exit Granted"""
]
ParserVersion = "v1.0.0"

s-nasuni-file-operations = {
  Vendor = Nasuni
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Fields = [
    """({access}[^,]+),([^,]*,){2}(({domain}[^,\\]+)[\\]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?),([^,]*,){2}("[^"]+"|[^,]*),[^,]*,({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """({src_file_dir}[^,]+\/+)?({src_file_name}[^,\/]+),[^,]+,([^,"]*,){3}("[^"]+"|[^,]*),CIFS,""",
    """({file_path}[^,]+),([^,"]*,){4}("[^"]+"|[^,]*),CIFS,""",
    """(({file_dir}[^,]+)[\/]+)?({file_name}[^\/,]+?(\.({file_ext}[^\/,\.]+))?),([^,"]*,){4}("[^"]+"|[^,]*),CIFS,""",
    """({file_path}[^,]+),([^,"]*,){3}("[^"]+"|[^,]*),CIFS,""",
    """(({file_dir}[^,]+)[\/]+)?({file_name}[^\/,]+?(\.({file_ext}[^\/,\.]+))?),([^,"]*,){3}("[^"]+"|[^,]*),CIFS,""",
  ]
  DupFields = [ "host->dest_host" 
}
```