#### Parser Content
```Java
{
Name = imperva-securesphere-kv-database-login-success-login
Vendor = "Imperva"
Product = "Imperva SecureSphere"
TimeFormat = "epoch"
Conditions = [
  """|Imperva|SecureSphere DAM|"""
  """cs5=Login"""
  """outcome=True"""
]
Fields = [
  """\srt=({time}\d+)"""
  """\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\sdvchost=({host}[^\s]+)"""
  """\sduser=({user}.+?)\s+\w+="""
  """\scs4=(?: |({app}.+?))\s+\w+="""
  """\scs3=(?: |({service_name}.+?))\s+\w+="""
  """\scs2=(?: |({server_group}.+?))\s+\w+="""
  """\sflexString1=(?: |({db_name}.+?))\s+\w+="""
  """\ssrc=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\sdst=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\sshost=({src_host}[^\s]+)"""
  """\sdhost=({dest_host}[^\s]+)"""
]
ParserVersion = "v1.0.0"


}
```