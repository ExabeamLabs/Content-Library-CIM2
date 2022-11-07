#### Parser Content
```Java
{
Name = microsoft-mcas-cef-file-write-success-appidonedrive
Vendor = Microsoft
Product = Cloud App Security (MCAS)
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """cs2=APPID_ONEDRIVE"""
  """|MCAS|SIEM_Agent|"""
]
Fields = [
  """SIEM_Agent\|[^|]+?\|({access}[^\|]+)\|"""
  """msg=(.+?):\s*({file_type}[^\s]+)\s+({file_dir}[^=]+)[\\\/]+(|({src_file_name}.*?({src_file_ext}\.[^\\:\s.]+)?))\s+(?:$|\w+=)"""
  """\ssuser=({user}[^@]+)@([\.\w+]+\.)?({email_domain}[^\.\s]+\.(?:com|net|info|edu|org|gov|co|jp|ru|de|ir|it|in|fr|info|pl|nl|es|gr|cz|eu|tv|me|jp|ca|cn|uk|my|cc|id|us|nz|biz|club|io|gg|fi|au|st|tw|asia|sg|ie|li|za|ch))\s+"""
  """\srt=({time}\d+)"""
  """\sdestinationServiceName =({app}.+?)\s+\w+="""
  """\srequestClientApplication=(|({user_agent}.+?))\s+\w+="""
  """\sdvc=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
]
ParserVersion = "v1.0.0"


}
```