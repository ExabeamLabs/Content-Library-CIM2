# Code Changes for crowdstrike-falcon-app-activity-fail-win-1 (Event Builder)

| Code Change | Field Name | 2025.14.1 | 2025.15.1 |
|-------------|------------|-----------|------------|
| edit_conditions | expression | InList(type, 'crowdstrike-falcon-sk4-app-activity-awsec2networkinterface') and InList(toLower(result), 'false') containsAny(toLower(os), 'win') | InList(type, 'crowdstrike-falcon-sk4-app-activity-awsec2networkinterface') and InList(toLower(result), 'false') && containsAny(toLower(os), 'win') |