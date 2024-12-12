#### Parser Content
```Java
{
Name = microsoft-mdhcplog-json-dns-record-create-fail-forwardrecord
 Conditions = [""""LogName":"DhcpAdminEvents"""", """"ProviderName":"Microsoft-Windows-DHCP-Server"""", """"MachineName":""", """"Properties":""", """"Message":""", """Forward record registration for IPv4 address"""]
 ParserVersion = v1.0.0
 Fields = ${DLWindowsParsersTemplates.json-microsoft-windows-dhcp-events.Fields}[
   """"MachineName":"({host}[\w.-]+)""""
 ]

json-microsoft-windows-dhcp-events = {
  Vendor = Microsoft
  Product = Microsoft DHCP Log
  TimeFormat = "epoch"
  Fields = [
   """"TimeCreated":"\\\/Date\(({time}\d{13})""",
   """"LogName":"({event_name}[^"]+)"""",
   """UserId[^=]+?Value":"({user_sid}[^"]+)[^:]+?,"TimeCreated""""
   """"Message":"({additional_info}[^"]+)"""",
  
}
```