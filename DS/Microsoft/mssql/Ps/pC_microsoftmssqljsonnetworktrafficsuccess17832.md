#### Parser Content
```Java
{
Name = microsoft-mssql-json-network-traffic-success-17832
  ParserVersion = v1.0.0
  Conditions = [ """"provider_name":"MSSQLSERVER"""", """"message":"""", """"host":"""" ]

exalms-sqlserver-events {
    Vendor = Microsoft
    Product = MSSQL
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """"@timestamp"\s*:\s*"({time}[^"]+)"""",
      """"computer_name"\s*:\s*"({host}[\w.-]+?)"""",
      """CLIENT:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
      """({app}MSSQLSERVER)""",
      """"message":"({additional_info}[^"]+)"""
    
}
```