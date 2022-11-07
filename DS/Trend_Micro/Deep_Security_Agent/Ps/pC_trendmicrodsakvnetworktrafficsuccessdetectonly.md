#### Parser Content
```Java
{
Name = trendmicro-dsa-kv-network-traffic-success-detectonly
Vendor = "Trend Micro"
Product = "Deep Security Agent"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Fields = [
  """\d\d:\d\d\s({host}.+?)\sCEF:"""
  """proto=({protocol}.+?)(\s+\w+=|\s*$)"""
  """in=({bytes_in}\d+)"""
  """out=({bytes_out}\d+)"""
  """dst=({dest_ip}[^\s]+)"""
  """src=({src_ip}[^\s]+)"""
  """dmac=({dest_mac}[^\s]+)"""
  """smac=({src_mac}[^\s]+)"""
  """dvchost=({dest_host}[^\s]+)"""
  """cs2=({method}[^\s]+)"""
  """CEF.*?\|(.*?\|){4}({rule}.+?)\|"""
  """dpt=({dest_port}\d+)"""
  """spt=({src_port}\d+)"""
  """cs1=({additional_info}.+?)\s\w+="""
  """suser=(NT AUTHORITY\\+SYSTEM|({user}[^\s]+))"""
  """fileHash=({file_hash}[^\s]+)"""
  """act=({operation}[^\s]+)"""
  """cs3=({hash_md5}[^\s]+)"""
  """cs2=({hash_sha1}[^\s]+)"""
  """suid=({suid}.+?)\s\w+="""
  """filePath=({file_path}({file_dir}[^,]*?)[\\\/]*({file_name}[^\\]+?(\.({file_ext}[^\.\s]+))?))\s\w+="""
]
Conditions = [
  """|Trend Micro|Deep Security Agent|"""
  """act=detectOnly"""
  """CEF:"""
]
ParserVersion = "v1.0.0"


}
```