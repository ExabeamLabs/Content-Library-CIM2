#### Parser Content
```Java
{
Name = "zeek-z-str-http-session-custom"
Vendor = "Zeek"
Product = "Zeek"
TimeFormat = "epoch_sec"
Conditions = [
  """<custom-condition>"""
]
Fields = [
  """^[^\t]*?({time}\d{10})\.\d+\t"""
  """^[^\t]*?\t({host}[^\t]+)"""
  """^[^\t]*?\t[^\t]+\t({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """^[^\t]*?\t([^\t]+\t){2}({src_port}\d+)"""
  """^[^\t]*?\t([^\t]+\t){3}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """^[^\t]*?\t([^\t]+\t){4}({dest_port}\d+)"""
  """^[^\t]*?\t([^\t]+\t){6}({method}\w+)"""
  """^[^\t]*?\t([^\t]+\t){7}({web_domain}[^\t]+)"""
  """^[^\t]*?\t([^\t]+\t){8}({uri_path}[^\t\?]+)({uri_query}\?[^\t]+)?"""
  """^[^\t]*?\t([^\t]+\t){10}Mozilla\/.+\((({os}iOS|Android|BlackBerry|Windows Phone|BeOS|(?:X|x)11|(?:W|w)indows|(?:L|l)inux|(?:M|m)acintosh|(?:D|d)arwin).+?({browser}Chrome|Safari|Opera|(?:F|f)irefox|MSIE|Trident))"""
  """^[^\t]*?\t([^\t]+\t){13}({http_response_code}\d+)"""
  """^[^\t]*?\t([^\t]+\t){14}({result}(-|[^\t]+))"""
  """^[^\t]*?\t([^\t]+\t){25}\s*({mime}[^\t]+?)\s*"""
]
ParserVersion = "v1.0.0"


}
```