## The CIA Triad

The **CIA triad** is a foundational model in information security that defines the three core objectives of secure system design: **Confidentiality, Integrity, and Availability**. It acts as a guiding framework for evaluating security controls and decisions. If a security measure does not clearly support at least one of these principles, its value should be questioned.

### Confidentiality
Confidentiality ensures that information is accessible only to authorized individuals or systems. The goal is controlled access, not secrecy for its own sake. Common mechanisms include authentication, authorization, encryption, and network segmentation. Breaches of confidentiality occur when sensitive data is exposed to unauthorized parties, such as through leaked credentials, exposed databases, or misconfigured cloud storage.

### Integrity
Integrity focuses on maintaining the accuracy, consistency, and trustworthiness of data throughout its lifecycle. Data should only be modified in authorized and traceable ways. Unauthorized changes to records, source code, or configurations represent integrity failures, even if the system remains operational. Techniques such as hashing, digital signatures, checksums, access controls, and audit logs help preserve data integrity.

### Availability
Availability ensures that systems, services, and data are accessible to authorized users when needed. A system that is secure but frequently unavailable fails its purpose. Threats to availability include hardware failures, denial-of-service attacks, software bugs, and natural disasters. Redundancy, backups, load balancing, failover strategies, and disaster recovery planning are key to maintaining availability.

### Balancing the Triad
The CIA triad is about balance, not maximizing a single objective. Strengthening one aspect can sometimes weaken another—for example, strict access controls may reduce usability or availability. Effective security design carefully manages these trade-offs to meet the system’s real-world requirements.
