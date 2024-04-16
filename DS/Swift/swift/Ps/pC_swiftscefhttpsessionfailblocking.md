#### Parser Content
```Java
{
Name = "swift-s-cef-http-session-fail-blocking"
Vendor = "Swift"
Product = "Swift"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
Conditions = [
"""SocketChannelEndPoint"""
"""SslConnection"""
"""HttpConnection"""
"""BLOCKING"""
]
Fields = [      
	    """\d\d:\d\d:\d\d\s*({host}[\w\-\.]+)\s*""",
      """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+)""",
      """l=\/?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """r=\/?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """uri=({url}[^,]+)""",
      """rs=({action}[^\s]+)\s"""
]
ParserVersion = "v1.0.0"


}
```