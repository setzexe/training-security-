# Resiliency

Resiliency refers to the concept of designing systems so that when things eventually break or get attacked (they will. No system is invincible), the entire system does not get destroyed *especially* for long periods of time. Resilience is the backbone of availability.

## High Availability (HA) & Clustering

High availability keeps backup gear powered on, configured, and ready immediately if something wrong were to occur. This does not refer to all backups or resilience gear, only high quality equipment that would be ready almost instantly.

**Server clustering** uses this concept. Multiple physical servers are grouped together so that they look like one server from the outside. But if one server were to go down, the other servers could easily take over for it as if nothing had happened.

**Load balancers** help with this concept by checking the health and resources of a server. If a node (server) were to fail its health check, resources or traffic can be routed to available servers instead.

This is very expensive and can only really be done by very financially capable businesses.

## Site Resiliency (Hot, Warm, or Cold)

These are backup locations / systems for resilience in case of emergency. They can be measured by temperature:

**Hot sites** have high availability and duplicate services for its main services. This can be extremely costly, but immediate and effective.

**Warm sites** are like the skeleton of hot sites; you have the backup tools available, but you would have to manually power these / feed these backup data. This is a proper middle grounds for most businesses.

**Cold sites** are very barren. They hold no backup tools or data and only have power, data, and AC. You start from near fresh. This is not ideal, but is used in cases where immediate systems are not necessary.

## Platform Diversity

Businesses should never run their servers on the same system, OS, vendor, architecture, etc. The reason for this is that in cases where an attack happens, an attacker being on the exact same path could potentially damage the entire system. This is especially bad on zero day; if a business uses Windows for everything and a zero day Windows vulnerability is discovered, that business might be done for.

It is common to run Linux and Windows on backend servers, with common user OS's (Windows and macOS) running on client endpoints.

Although great security practice, this would involve a bit more expertise from internal staff.

## Multi-Cloud Architecture

Splitting workloads across multiple independant service cloud providers (Azure, AWS, Google Cloud) is the cloud version of this concept. Even cloud suffers from outages (actually, more than physical servers).

## Continuity of Operations Planning (COOP) and Non-Technical Fallbacks

These are documented procedures used by businesses to keep things going when *all* technology fails. Suppose a restaurants food ordering system goes down. The fallback might be simply taking orders in pen and paper, and then paying in cash.
