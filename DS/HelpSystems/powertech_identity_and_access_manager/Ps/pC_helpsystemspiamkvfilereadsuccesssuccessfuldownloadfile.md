#### Parser Content
```Java
{
Name = "helpsystems-piam-kv-file-read-success-successfuldownloadfile"
ParserVersion = "v1.0.0"
Vendor = "HelpSystems"
Product = "Powertech Identity and Access Manager"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """sshftl_download_ok"""
  """Successful download of file"""
]
Fields = [
  """clientTime="*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)Z\"*"""
  """\d\dZ\s+({host}[\w\-.]+)\s+(scp|sftp) - sshftl_download_ok"""
  """user="*({user}[\w\.\-]{1,40}\$?)""""
  """Successful download of file ({file_path}.+?) to """
  """Successful download of file (?:({file_dir}(\/[^\/]+)*\/))?({file_name}[^\/.]+\.?({file_ext}[^\/]*)) to """
  """fromhost="*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """({event_code}sshftl_download_ok)"""
]
DupFields = [
  "host->dest_host"
 ]


}
```