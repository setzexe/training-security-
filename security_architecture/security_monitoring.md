# Security Monitoring

Attacks can happen at any point at any day. Monitoring must be 24/7/365 at ideally every entry point: user logins, publically available services, data storage, remote access connections, etc. When something looks wrong, you react accordingly. Status dashboards are an interactive way of working with monitoring.

## Monitoring Computing Resources

- Systems: Watch for authentication that does not make sense, like a user logging in from a strange location. Watch servers for unusual activity, check that backups are completing, and confirm software versions are current.
- Applications: Monitor availability / how the app is running. Malicious data transfers and security notifications are huge signs to look out for.
- Infrastructure: Watch connections and remote access systems. Review firewall and IPS reports for a rise in traffic or how often certain things may be happening (early sign of being targeted).

## Log Aggregation (SIEM)

Every system creates its own logs, and checking each one seperately is time consuming. A **SIEM (Security Information and Event Management)** system collects all these logs and showcases them on a central console, allowing one to easily track different things like application access, data transfers, locations of attackrs, etc., centrally.

## Scanning

Monitoring is not only passive log collecting, Active scans on systems and devices gather details like operating systems, drivers, or anomalies that may look out of place. This scanned activity can actually be fed to a SIEM to understand it more.

## Reporting

When data is collected, it should be reported properly so the user understands what to do with it. The user knows what the information is, and how to proceed forward quickly.

## Archiving

Breaches often are not discovered immediately. Some breaches dont go unnoticed for years, and monitoring may only go back weeks. This makes archiving monitoring logs / data important. The retention period is often required by law or some organizational policy.

## Alerting

Alerts are real-time notifications of security events. These should be built on actionable, up-to-date data. Setting up alerts involve two choices; how they are delivered (email, SMS, a security console), and the alarm threshold (what desides when something is alarm worthy). When an alert fires, one common response is quarantining the affected service or system.

**Alert turning** adjusts rules over time to cut down on false positives and false negatives, basically tuning your alert system so it truly knows what to alert for.
