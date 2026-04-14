# Code Changes for zscaler-pa-json-vpn-login-success-doubleencryption (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | bytes_in |  | ['ZENTotalBytesRxConnector":\s*({bytes_in}\d+),', 'exa_regex=ZENTotalBytesRxConnector":\s*({bytes_in}\d+),'] |
| edit_regex_field | bytes_out |  | ['ZENTotalBytesTxConnector":\s*({bytes_out}\d+),', 'exa_regex=ZENTotalBytesTxConnector":\s*({bytes_out}\d+),'] |