An analyst needs to dismiss false positives while responding to true positives

Conditional Analysis - A simple form of correlation performed by a machine by using signature detection and rules-based policies
Conditional analysis used a signature or rule to generate an alert (IF x AND (y OR z))
Conditional analysis creates large numbers of false positives and cannot find zero-day or new TTPs

Heuristic Analysis - A method that uses feature comparisons and likenesses rather than specific signature matching to identify whether the target of observation is malicious
Heuristic analysis uses machine learning to alert on behavior that is similar enough to a signature or rule
Machine Learning - A component of AI that enables a machine to develop strategies for solving a task given a labeled data set where features have been manually identified but without further explicit instructions
Over time, your heuristics get much better when they have a good trained data set

Behavioral Analysis - A network monitoring system that detects changes in normal operating data sequences and identifies abnormal sequences
Behavioral analysis generates an alert whenever anything deviates outside a defined level of tolerance from a given baseline
Behavioral analysis generates a lot of false positives and false negatives until its statistical model is adequately trained and tuned

Anomaly Analysis - A network monitoring system that uses a baseline of acceptable outcomes or event patterns to identify events that fall outside the acceptable range
Anomaly analysis generates an alert on any event or outcome that doesn't follow a set pattern

Anomaly Analysis vs Behavioral Analysis:
- Anomaly - Uses prescribed patterns (like an RFC or industry standard)
- Records expected patterns in relation to the device(s) being monitored

