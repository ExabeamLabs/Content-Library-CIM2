#### Parser Content
```Java
{
Name = microsoft-mcas-cef-file-write-success-appidonedrive
Vendor = Microsoft
Product = Microsoft CAS
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """cs2=APPID_ONEDRIVE"""
  """|MCAS|SIEM_Agent|"""
]
Fields = [
  """SIEM_Agent\|[^|]+?\|({access}[^\|]+)\|"""
  """msg=(.+?):\s*({file_type}[^\s]+)\s+({file_dir}[^=]+)[\\\/]+(|({src_file_name}.*?({src_file_ext}\.[^\\:\s.]+)?))\s+(?:$|\w+=)"""
  """\ssuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)@([\.\w+]+\.)?({email_domain}[^\.\s]+\.(?:com|net|info|edu|org|gov|co|jp|ru|de|ir|it|in|fr|info|pl|nl|es|gr|cz|eu|tv|me|jp|ca|cn|uk|my|cc|id|us|nz|biz|club|io|gg|fi|au|st|tw|asia|sg|ie|li|za|ch))\s+"""
  """\srt=({time}\d{13})"""
  """destinationServiceName =({app}.+?)\s+\w+="""
  """\srequestClientApplication=(|({user_agent}.+?))\s+\w+="""
  """\sdvc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """Add user to group in site:\s?user\s?({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\s?to group\s?({group_name}[^=]+)\s?suser"""
]
ParserVersion = "v1.0.0"


}
```