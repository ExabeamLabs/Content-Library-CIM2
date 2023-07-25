#### Parser Content
```Java
{
Name = microsoft-mdhcplog-json-dns-record-modify-success-operational
 Conditions = [""""LogName":"Microsoft-Windows-Dhcp-Server/Operational"""", """"MachineName":""", """"Properties":""", """"Message":"""]
 ParserVersion = v1.0.0

json-microsoft-windows-dhcp-events = {
  Vendor = Microsoft
  Product = Microsoft DHCP Log
  TimeFormat = "epoch"
  Fields = [
   """"TimeCreated":"\\\/Date\(({time}\d{13})""",
   """"MachineName":"({host}[\w.-]+)"""",
   """"LogName":"({event_name}[^"]+)"""",
   """UserId[^=]+?Value":"({user_sid}[^"]+)[^:]+?,"TimeCreated""""
   """"Message":"({additional_info}[^"]+)"""",
  
}
```