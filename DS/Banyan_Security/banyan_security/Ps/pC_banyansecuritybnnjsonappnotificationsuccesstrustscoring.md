#### Parser Content
```Java
{
Name = banyansecurity-bnn-json-app-notification-success-trustscoring
  ParserVersion = "v1.0.0"
  Conditions = [ """"type":""", """"TrustScoring"""", """"action":""", """"sub_type":""", """"Device"""" ]

banyan-events  = {
    Vendor = Banyan Security
    Product = Banyan Security
    TimeFormat = "epoch"
    Fields = [
      """created_at":\s*({time}\d{13})""",
      """"host_name":\s*"({dest_host}[^":]+)""",
      """"host_ip":\s*"(({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""",
      """"client":[^\}]+"ip_address":\s*"(-|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""",
      """"user":\s*\{[^\{\}]*?"name":\s*"({full_name}[^"]+)""",
      """"user":\s*\{[^\{\}]*?"email":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""",
      """"type":\s*"({event_category}[^"]+)",\s*"sub_type":\s*"({operation_type}[^"]+)""",
      """"action":\s*"({operation}[^"]+)""",
      """"roles":\s*\[({access}[^\]]+)""",
      """"groups":\s*\[({groups}[^\]]+)""",
      """"message":\s*"({additional_info}[^"]+)""",
      """"user_agent":\s*"({user_agent}[^"]+)"""
    
}
```