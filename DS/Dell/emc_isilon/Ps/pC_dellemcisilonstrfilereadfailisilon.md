#### Parser Content
```Java
{
Name = dell-emcisilon-str-file-read-fail-isilon
  Conditions = [ """ Isilon""", """|FAILED:""" ]
  ParserVersion = "v1.0.0"

isilon-file-activity-1 = {
  Vendor = Dell
  Product = EMC Isilon
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+[\+\-]+\d+:\d+)""",
    """\d+-\d+-\d+T\d+:\d+:\d+[\+\-]+\d+:\d+\s+({host}[\w\-.]+)\s""",
    """({user_sid}[^\s\|:\]]+)\|([^\|]*\|){3}({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\|({protocol}[^\|]+)\|({access}[^\|]+)\|({result}SUCCESS|FAILED)(:({failure_code}[^\|]*))?\|([^\|]*\|)?({file_type}FILE|DIR)\|"""
    """\|({file_path}({file_dir}[^"\|][^\|,]*?[\\\/]+)?(|({file_name}[^\\\/\|]*?(\.({file_ext}\w+))?)))\s*$"""
    """\|FAILED:.*?\|(FILE|DIR)\|({failure_reason}[^\|]+)""",
  
}
```