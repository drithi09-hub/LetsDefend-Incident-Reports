# Lessons Learned

- Event ID 4625 indicates a failed Windows logon.
- Event ID 4624 indicates a successful Windows logon.
- Repeated failed RDP logins from the same external IP may indicate a brute-force attack.
- Default usernames such as "admin" and "guest" are commonly targeted by attackers.
- Firewall logs help confirm repeated connection attempts to RDP services.
- Always verify whether a successful login occurred before concluding the attack was successful.