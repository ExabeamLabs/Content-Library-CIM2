#### Parser Content
```Java
{
Name = zeek-z-str-http-session-httpeth0log
  ParserVersion = v1.0.0
  Vendor = Zeek
  Product = Zeek
  TimeFormat = "epoch_sec"
  Conditions = [ """/http_eth0.log""" ]
  Fields = [
    """({time}\d{10})\.\d{6}\s+({connection_id}[^\s]+)\s+(?:-|(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|[^\s]+))\s+(?:-|(({src_port}\d+?)|[^\s]+))\s+(?:-|(({dest_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|[^\s]+))\s+(?:-|(({dest_port}\d+?)|[^\s]+))\s+(?:-|([^\s]+))\s+(?:-|({method}[^\s]+))\s+(?:-|([^\s]+))\s+([^\s]+)\s+(?:-|({referrer}[^\s]+))\s+.*?\((?:-|({user_agent}[^\s]+))\)\s+(?:-|([^\s]+))\s+(?:-|([^\s]+))\s+(?:-|({http_response_code}\d+))\s+(?:-|([^\s]+))\s+""",
   """({time}\d{10})\.\d{6}\s+({connection_id}[^\s]+)\s+(?:-|(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|[^\s]+))\s+(?:-|(({src_port}\d+?)|[^\s]+))\s+(?:-|(({dest_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|[^\s]+))\s+(?:-|(({dest_port}\d+?)|[^\s]+))\s+(?:-|([^\s]+))\s+(?:-|({method}[^\s]+))\s+(?:-|([^\s]+))\s+([^\s]+)\s+(?:-|({referrer}[^\s]+))\s+(?:-|({user_agent}[^\s]+))\s+(?:-|([^\s]+))\s+(?:-|([^\s]+))\s+(?:-|({http_response_code}\d+))\s+(?:-|({status_msg}[^\s]+))\s+(?:-|([^\s]+))\s+(?:-|([^\s]+))\s+(?:-|({orig_filenames}[^\s]+))\s+(?:-|(\(empty\))|({tags}[^\s]+))\s+(?:-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+(?:-|([^\s]+))\s+(?:-|({proxied}[^\s]+))\s+(?:-|([^\s]+))\s+(?:-|([^\s]+))\s+(?:-|([^\s]+))\s+(?:-|({mime}[^\s]+?))\s*""",
    """\d{10}\.\d{6}\s+([^\s]+\s+){7}(?:-|(?!(\d{1,3}\.){3}\d{1,3})({web_domain}.+?))\s*\t([^\s]+\s+){16}(?:-|({mime}[^\s]+))\s*""",
    """\d{10}\.\d{6}\s+([^\s]+\s+){8}(?:-|({uri_path}[^\s\?]+)(\?({uri_query}[^\s]+))?)""",
    """({protocol}http)"""
  ]


}
```