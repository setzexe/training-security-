# Segmentation (Segmenting the Network)

This is a common idea in the world of STEM as a whole; segmenting big things into parts might make it a lot easier to work with and handle. Breaking down a network into different segments with different utilities could make handling these alot easier. This can include with devices, VLANs, virtual networks, and just individual parts of those networks. Doing this can directly help with performance too; if parts do not have to move across the whole system to get to each other, perhaps the system can run smoother.

It should be noted that security should still be kind of a foundational layer for the rest of segmentation; maybe each segmentation will have different implementations of security, but security still should be a priority. Similarly, this segmentation can help make security related tasks easier for people. For example, telling users to use applications within the database segment (to talk to the database) would be a lot safer then asking the employees to talk to it directly each time.

Sometimes segmentation is mandatory for security / change / procedure purposes. Many organizations want financial details as a segment away from any important segments.

## Access Control List

These are lists that just allow or disallow traffic. You can toggle (in groups if needed);
- Source IP & Destination IP (essential restricting access to network devices)
  - This could prevent non-admin access when needed
- Port Number
- Time of Day
- Application
- Much more...

Take all groups in account. It is very much possible to lock yourself out.

Many operating systems use **ACLs** to provide file access. Groups and the user system are an example within organizations.

## Application Allow / Deny List

Any application can be dangerous due to vulnerabilities or malware / trojans. This is similar to ACLs except with applications; you can control what apps can and can't be used. While many lists contain both allow AND deny, organizations might only have one or the other:

- Allow
  - Very restrictive; only apps on that list can be used. No other app.
- Deny
  - Only apps on that list are restricted. Typically used on vulnerable apps.

This can be as simple as a module, but there are other ways these allow / deny lists exist.

**Application hash's** only run if the hash matches the correct logged hash. Change in the file = change in the hash = potential vulnerability = locked.

**Certificates** verify integrity and non-repudian, making these 99.9% trustable.

**Network zone's** only allow apps to be run in a particular network. **Path access** means that only applications under the filepath (/User/importantApps/... for example).