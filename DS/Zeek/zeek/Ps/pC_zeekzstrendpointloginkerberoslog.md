#### Parser Content
```Java
{
Name = zeek-z-str-endpoint-login-kerberoslog
  ParserVersion = v1.0.0
  Vendor = Zeek
  Product = Zeek
  TimeFormat = "epoch_sec"
  expiry_timeFormat = ["epoch_sec"]
  issue_timeFormat = ["yyyy-MM-dd HH:mm:ss"]
  Conditions = [ """/kerberos.log""" ]
  Fields = [
    """({time}\d{10})\.\d{6}\s+({connection_id}[^\s]+)\s+(?:-|(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|[^\s]+))\s+(?:-|(({src_port}\d+?)|[^\s]+))\s+(?:-|(({dest_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|[^\s]+))\s+(?:-|(({dest_port}\d+?)|[^\s]+))\s+(?:-|({request_type}[^\s]+))\s+(?:-|([^\s]+))\s+(?:-|({service_name}[^\/\s]+)).+?\s+(?:-|({result}[^\s]+))\s+(?:-|({result_code}[^\s]+))\s+(?:-|({issue_time}[^\s]+))\s+(?:-|({expiry_time}\d{10})\.\d+)\s+(?:-|({ticket_encryption_type}[^\s]+))\s+({ticket_options}[^\s]+\s+[^\s]+)\s+(?:-|({client_cert_subject}[^\s]+))\s+(?:-|([^\s]+))\s+(?:-|({server_cert_subject}[^\s]+))\s+(?:-|([^\s]+?))\s*"""
    """\d{10}\.\d{6}\s+([^\s]+\s+){6}({user}[\w\.\-]{1,40}\$?)\/({domain}[^\s]+)\s*""",
    """\d{10}\.\d{6}\t([^\s]+\s+){7}({dest_host}[^\/]+)\\"""
  ]


}
```