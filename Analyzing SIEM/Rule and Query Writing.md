Correlation - Interpretation of the relationship between individual data points to diagnose incidents of significance to the security team

Correlation rule - A statement that matches certain conditions as expressed using logical expressions, such as AND and OR, and operations such as == (equals/matches), < (less than), > (greater than), and in (contains)

A rule can be created to send an alert if multiple user log-on failures occur within one hour from a single account. This may look something like:
`Error.LogonFailure > 3 AND LogonFailure.User AND Duration < 1 hour`

Correlation rules depend on normalized data. Correlation rules match data as it is ingested into a SIEM and requires data in memory as persistent state data

SIEM Queries - Extracts records from among all the data stored for review or to show as a visualization

Correlation Rules - It will flag an alert immediately
SIEM Queries - It waits until you run the query and look for that information

An example SIEM query that would be similar to the rule mentioned above might look like:
`Select (User) Where (Error.LogonFailure > 3 AND LogonFailure.User AND Duration < 1 hour) Sorted By (date, time)`

