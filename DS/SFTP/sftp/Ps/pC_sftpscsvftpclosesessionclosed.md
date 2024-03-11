#### Parser Content
```Java
{
Name = sftp-s-csv-ftp-close-sessionclosed
  Vendor = SFTP
  Product = SFTP
  ParserVersion = "v1.0.0"
  Conditions = [ """ sftp-""", """"Session Closed"""" ]

sftp-events-1 = {
  Vendor = SFTP
  Product = SFTP
  TimeFormat = "EEE ddMMMyy HH:mm:ss"
  Fields = [
    """({host}[\w\-.]+)\s+sftp-[^",]+"({time}\w+\s+\d+\w+\d+\s+\d\d:\d\d:\d\d)""",
    """ sftp-.*?("[^"]*",){1}"({action}[^",]+)"""",
    """ sftp-.*?("[^"]*",){2}"(|({user}[^",\s]+))"""",
    """ sftp-.*?("[^"]*",){3}"(|({src_host}[\w\-.]+))"""",
    """ sftp-.*?("[^"]*",){4}"(|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""",
    """ sftp-.*?("[^"]*",){5}"(|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""",
    """ sftp-.*?("[^"]*",){6}"(|({dest_port}\d+))"""",
    """ sftp-.*?("[^"]*",){8}"(|({file_path}({file_dir}[^"]*?)[\\\/]*({file_name}[^\\"]+?(\.({file_ext}[^\.\s"]+))?)))"""",
    """ sftp-.*?("[^"]*",){9}"(|({bytes}\d+))"""",
    """ sftp-.*?("[^"]*",){11}"(|({user_agent}[^"]+))"""",
  ]
  DupFields = [ "host->dest_host" 
}
```