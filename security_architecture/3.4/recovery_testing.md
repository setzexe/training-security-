# Recovery Testing

Recovery testing is how teams verify that disaster recovery (DR) plans work and that recovery systems execute properly when an actual emergency hits. Plans mean nothing if the recovery system itself fails.

**Failure is mostly inevitable for business systems. It will happen at least once.** Plan for the absolute worst. As mentioned earlier, available / multiple components via things like clustering or load baring can help keep a server running if the worst were to happen.

**Parallel processing** can help in times of recovery. This is similar to load balancing and server clustering, except with resources like your processor. Multiple processors in one computer, or multiple computers. If one were to go down, processing could be diverted to other sources.

## Testing Methodologies

### Tabletop Exercise

Team members sit around a table and verbally talk about a hypothetical crisis step by step. This helps analysis alot and can help the planning of recovery testing. However, this has zero operational impact as no systems are effected.

### Structured Walkthrough

This involves reviewing the recovery plan itself line by line to find outdated / broken procedures. This is ideal.

### Simulation

Teams practice technical procedures against a mock incident. This is usually done in an isolated environment or sandbox like a Virtual Machine. This usually has very low impact on systems but remains highly effective because it directly tests a mock of the system. Phishing simulations are common for this.
