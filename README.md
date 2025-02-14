# BUILD-A-TOOL-TO-MONITOR-CHANGES-IN-FILES-BY-CALCULATING-AND-COMPARING-HASH-VALUES.
This Python-based tool is designed to monitor files for integrity by calculating and comparing hash values. It helps ensure that the content of a file has not been modified, either due to accidental changes, corruption, or unauthorized tampering. The tool regularly checks the file's hash and alerts users if any alterations are detected.

KEY FEATURES:
File Hashing: The tool calculates a cryptographic hash (e.g., SHA-256) of a given file. A hash function generates a unique string (hash) for the content of the file. Even a small change in the file will produce a completely different hash.

Regular Monitoring: The tool runs continuously and checks the file at specified intervals. It compares the current hash of the file with the previously stored hash.

Change Detection: If the current hash differs from the previous hash, the tool alerts the user, indicating that the file has been modified. If no change is detected, it simply confirms that the file remains intact.

Customizable Parameters:

Hash Algorithm: Users can choose from different cryptographic hash algorithms such as SHA-256, MD5, SHA-1, etc.
Check Interval: The time interval between each check can be adjusted, allowing the user to monitor files as frequently as needed (e.g., every 10 seconds, every minute).
Cross-platform Compatibility: The tool is built using Python, making it platform-independent. It can run on Windows, macOS, and Linux.

HOW IT WORKS:
Initial Setup:

The tool calculates the initial hash of the specified file (e.g., example.txt).
The hash is stored for future comparisons.
Monitoring Process:

The tool enters a loop, where it repeatedly calculates the current hash of the file at regular intervals.
If the file has been modified, the hash will change, and the tool will notify the user that the file has been altered.
Alert Mechanism:

When a change is detected (i.e., the current hash does not match the stored hash), the tool prints an alert message showing the previous and current hash values.
File Integrity Check:

The primary purpose of this tool is to ensure the integrity of files by detecting any unauthorized changes. This can be useful for monitoring configuration files, log files, sensitive data, or any files where integrity is critical.
Use Cases:
Security: Ensure that configuration files, source code, or sensitive documents have not been tampered with.
Backup Integrity: Verify that backup files remain unchanged over time.
Data Integrity: Ensure data has not been corrupted or altered during transfer or storage.
Audit Logging: Monitor log files for unauthorized modifications.
