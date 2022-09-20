#### Parser Content
```Java
{
Name = microsoft-mcas-cef-user-password-modify-success-changepassword
  Conditions = [ """CEF:""", """|MCAS|SIEM_Agent|""", """|Change password|""" ]
  ParserVersion = "v1.0.0"

cef-azure-onedrive-account-password = {
  Vendor = Microsoft
  Product = Cloud App Security (MCAS)
  TimeFormat = "epoch"
  Fields = [
    """\|SIEM_Agent\|[^\|]*\|[^\|]*\|({operation}[^\|]+)\|""",
    """\|SIEM_Agent\|[^\|]*\|({event_name}[^\|]+)\|""",
    """\Wrt=({time}\d+)""",
    """\Wdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\WdestinationServiceName =({app}.+?)\s+(\w+=|$)""",
    """\Wsuser=({user}[^@\s]+)\s+(\w+=|$)""",
    """\Wsuser=({email_address}[^@\s]+@[^@\s]+)\s+(\w+=|$)""",
    """\Wc6a1=\s*({src_ip}[A-Fa-f:\d.]+)""",
    """\Wmsg=({additional_info}.*?)\s+(\w+=|$)""",
  
}
```