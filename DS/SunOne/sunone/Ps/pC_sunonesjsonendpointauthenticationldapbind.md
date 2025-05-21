#### Parser Content
```Java
{
Name = "sunone-s-json-endpoint-authentication-ldapbind"
Vendor = "SunOne"
Product = "SunOne"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""authentication":"""
""""status":""""
""""network":""""
""""type":"ldap""""
"""LDAP bind without requesting signing"""
]
Fields = [
""""@timestamp":"({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)"""
""""index":"[^\{\}]*?"host":"({host}[\w\-.]+)"""
""""host":"({host}[\w\-.]+)"[^\{\}]*?"index":""""
""""status":"({result}[^"]+)"""
""""destination":\{.*?"ipv4":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
""""destination":\{.*?"host":"({dest_host}[\w\-.]+)"""
""""source":\{.*?"ipv4":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""source":\{.*?"host":"({src_host}[\w\-.]+)"""
""""user":\{?[^\{\}]*?"realm":"({realm}[^"\s]+)""""
""""user":\{?[^\{\}]*?"uid":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
""""message":"({additional_info}[^"]+)"""
""""domain":"({domain}[^"\s]+)"""
]
ParserVersion = "v1.0.0"


}
```