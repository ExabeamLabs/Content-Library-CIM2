#### Parser Content
```Java
{
Name = zeek-z-str-endpoint-login-ntlmlog
  ParserVersion = v1.0.0
  Vendor = Zeek
  Product = Zeek
  TimeFormat = "epoch_sec"
  Conditions = [ """/ntlm.log""" ]
  Fields = [
    """({time}\d{10})\.\d{6}\s+({connection_id}[^\s]+)\s+(?:-|(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|[^\s]+))\s+(?:-|(({src_port}\d+?)|[^\s]+))\s+(?:-|(({dest_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|[^\s]+))\s+(?:-|(({dest_port}\d+?)|[^\s]+))\s+(?:-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+(?:-|({src_host}[^\s]+))\s+(?:-|({domain}[^\s]+))\s+(?:-|({result}[^\s]+))\s+(?:-|({result_code}[^\s]+?))\s*"""
  ]


}
```