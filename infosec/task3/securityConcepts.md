# Security Through Obscurity

Security through obscurity is the practice of relying on secrecy rather than strong design to protect a system. This can include hiding source code, using non-standard protocols, obscuring URLs or endpoints, or assuming that attackers won’t discover how something works. While obscurity can delay low-effort or opportunistic attacks, it fails as a primary security strategy because modern attackers actively analyze, reverse-engineer, and probe systems.

Once the “secret” is discovered the protection collapses. Robust security assumes that an attacker knows how the system is built and still cannot compromise it. Obscurity may be used as a secondary layer, but never as the foundation of security.

# Attack Surface

The attack surface of a system is the total set of points where an attacker can interact with it, attempt exploitation, or extract information. This includes network ports, APIs, user inputs, authentication mechanisms, third-party libraries, hardware interfaces, and even human processes like password resets. A larger attack surface increases the likelihood of vulnerabilities simply because there are more components that can fail or be misconfigured. 

Reducing the attack surface should be practiced. Developers should disable unnecessary services, limit exposed functionality, apply least-privilege access, and simplify system design. Strong security engineering focuses not on hiding entry points, but on minimizing and hardening them so that even if they are visible, they remain resilient to attack.
