#### Parser Content
```Java
{
Name = zeek-z-str-ssh-traffic-success-sshlog
  ParserVersion = v1.0.0
  Vendor = Zeek
  Product = Zeek
  TimeFormat = "epoch_sec"
  Conditions = [ """/ssh.log""" ]
  Fields = [
    """({time}\d{10})\.\d{6}\s+({connection_id}[^\s]+)\s+(?:-|(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|[^\s]+))\s+(?:-|(({src_port}\d+?)|[^\s]+))\s+(?:-|(({dest_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|[^\s]+))\s+(?:-|(({dest_port}\d+?)|[^\s]+))\s+(?:-|({version}[^\s]+))\s+(?:-|({result}[^\s]+))\s+(?:-|({auth_attempts}[^\s]+))\s+(?:-|({direction}[^\s]+))\s+(?:-|({client_ssh_version}[^\s]+))\s+(?:-|({server_ssh_version}[^\s]+))\s+(?:-|({cipher}[^\s]+))\s+(?:-|({mac_alg}[^\s]+))\s+(?:-|(none)|({compression_algotithm}[^\s]+))\s+(?:-|({kex_alg}[^\s]+))\s+(?:-|({host_key_alg}[^\s]+))\s+(?:-|({host_key}[^\s]+))\s+(?:-|({remote_location_country_code}[^\s]+))\s+(?:-|({remote_location_region}[^\s]+))\s+(?:-|({remote_location_city}[^\s]+))\s+(?:-|({remote_location_latitude}[^\s]+))\s+(?:-|({remote_location_longitude}[^\s]+?))\s*""",
    """({time}\d{10})\.\d{6}\s+({connection_id}[^\s]+)\s+(?:-|(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|[^\s]+))\s+(?:-|(({src_port}\d+?)|[^\s]+))\s+(?:-|(({dest_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|[^\s]+))\s+(?:-|(({dest_port}\d+?)|[^\s]+))\s+(?:-|({version}[^\s]+))\s+(?:-|({result}[^\s]+))\s+(?:-|({direction}[^\s]+))\s+(?:-|({client_ssh_version}[^\s]+))\s+(?:-|({server_ssh_version}[^\s]+))\s+(?:-|({cipher}[^\s]+))\s+(?:-|({mac_alg}[^\s]+))\s+(?:-|(none)|({compression_algotithm}[^\s]+))\s+(?:-|({kex_alg}[^\s]+))\s+(?:-|({host_key_alg}[^\s]+))\s+(?:-|({host_key}[^\s]+))\s+(?:-|({remote_location_country_code}[^\s]+))\s+(?:-|({remote_location_region}[^\s]+))\s+(?:-|({remote_location_city}[^\s]+))\s+(?:-|({remote_location_latitude}[^\s]+))\s+(?:-|({remote_location_longitude}[^\s]+?))\s*"""
  ]
  DupFields = ["compression_algotithm->compression_alg"]


}
```